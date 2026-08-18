# CR10CORE

### Homemade large-format CoreXY 3D printer

> A fully custom, large-format CoreXY 3D printer, designed and built from scratch with one main constraint: **make it as good as possible, for as little money as possible.**

![CR10CORE](Documentation/images/cr10core.jpg)

---

##  MY story

This is the project that occupied **almost every evening of my 2025–2026 year... and quite a few evenings before and after that.**

In 2025, I was an engineering student who had just failed my first year of preparatory studies. I was broke, but I had a 3D printer: a **Creality CR-10S Pro V2**.

It was already a fairly large printer (315mmx315mmx400mm) compared to something like an Ender 3, but I quickly started running into its limitations

i already heavily modified this one with much bigger motor, an enclosure and a direct drive extruder but was still limited by material printing (only petg and pla) and speed.

So I decided to build my own printer.

Not a Voron.Not a Bambu Lab.Not a Snapmaker.

the printer i wanted didn't existed yet, i was run by the idée : 

> **Build the best large-format printer I could, using what I already had : salvaged parts from my last printer and a lot of time.** 

What started as a way to get around the limitations of my CR-10S Pro V2 slowly turned into a much bigger project.

I designed the mechanics, experimented with different architectures, built custom electronics and firmware configurations, broke things, rebuilt them, measured them, redesigned them, and gradually turned a pile of inexpensive parts into a surprisingly capable machine.

And then something happened that I absolutely did not expect.

### One year later...

I presented the printer at the **Polytech3D Challenge**.

The machine ended up winning a prize and more importantly to me received recognition from several professionals in the 3D printing industry who were present at the event.


**This repository keep track of my last year of project.**

---

#  About the CR10CORE

CR10CORE is a **homemade large-format CoreXY 3D printer** designed very poorly by me 

The machine is built around:

* open source
* Verry customizable part
* CoreXY kinematics
* awd capability
* Large build volume
* Klipper firmware
* Custom mechanical components
* Custom electronics
* High-speed motion
* Automatic bed leveling
* Z-tilt
* Input Shaper
* Pressure Advance
* Custom toolhead system
* laser engraving/ cutting capability


The project intentionally prioritizes:

**Performance / Cost / Repairability / Modifiability**

---

##  Design philosophy

The project started with a few simple rules.

###  Keep the cost low

Whenever possible, I try to use:

* Standard hardware
* Cheap off-the-shelf components
* Reused parts
* Salvaged components
* 3D printed parts
* DIY solutions

###  Make it repairable

The printer is designed to be understood and repaired by its builder.

No proprietary ecosystem should be required to keep the machine running.

### Burning thing

Not every idea works.

This repository intentionally documents prototypes, failed designs, measurements and experiments instead of only showing the final result.

###  Design rather than assemble

The goal is not simply to assemble existing printer components.

Every part of the machine has been **designed specifically for this project**.

---

#  Specifications

> ⚠️ This section is currently being completed.

| Specification | CR10CORE |
| ------------- | -------- |
| Kinematics    | CoreXY   |
| Build volume  | TBD      |
| Firmware      | Klipper  |
| Mainboard     | TBD      |
| MCU           | TBD      |
| Extruder      | TBD      |
| Hotend        | TBD      |
| Motion system | TBD      |
| Input Shaper  | Yes      |
| Bed leveling  | Yes      |
| Toolchanger   | TBD      |
| Power supply  | TBD      |

---

#  Documentation

The documentation is being built alongside the machine.

###  Building the printer

to do 

###  Technical documentation

to do

###  Experiments & development

The `Research/` directory contains experiments, prototypes, calculations and design decisions made throughout the development of the printer.

---

# 🗺️ Project status

The CR10CORE is an evolving project.

| Subsystem     | Status            |
| ------------- | ----------------- |
| Frame         | 🟢 Functional     |
| CoreXY motion | 🟢 Functional     |
| AWD motion    | 🟢 Functional     |
| Z axis        | 🟢 Functional     |
| Extrusion     | 🟢 Functional     |
| Electronics   | 🟢 Functional     |
| Klipper       | 🟢 Functional     |
| Input Shaper  | 🟢 Tuned          |
| Bed leveling  | 🟢 Functional     |
| Toolchanger   | 🟡 In dev         |
| Documentation | 🟡 very late      |

> The status above will evolve as the project continues.

---

# 📸 Gallery

<!-- Add photos and videos of the printer here -->

---

#  Why publish the project?

This project started as a personal experiment but i will have to present it to student next year so its a great exercice to put 1 year of thought and dev into simple a git page

The project is also an attempt to document the **engineering process**, not just the final machine.

---

#  Contributing

CR10CORE is primarily a personal project but thaks to my friend who help me at some stage of the project

any ideas, improvements, bug reports and discussions are welcome.

If you find a mistake, have an improvement, or simply want to discuss a design choice, feel free to open an Issue or start a Discussion.


---

#  License

This project is open source. and will remain it. any fork should be with the same liscence

The specific license applying to the CAD files, hardware and software can be found in [`LICENSE`](LICENSE).

---

##  If you like the project

If you find CR10CORE interesting, consider giving the repository a ⭐ on GitHub.


---

**CR10CORE Built because the printer I wanted didn't existed**
