# CR10CORE

### Homemade large-format CoreXY 3D printer

> A fully custom, large-format CoreXY 3D printer, designed and built from scratch with one main constraint: **make it as good as possible, for as little money as possible.**

![CR10CORE](/image/20260626_155403.jpg)

---

##  about Me

This is the project that occupied **almost every evening of my 2025–2026 year... and quite a few evenings before and after that.**

In 2025, I was an engineering student who had just failed my first year of preparatory studies. I was broke, but I had a 3D printer: a **Creality CR-10S Pro V2**.

It was already a fairly large printer (315mmx315mmx400mm) compared to something like an Ender 3, but I quickly started running into its limitations

i already heavily modified this one with much bigger motor, an enclosure and a direct drive extruder but was still limited by material printing (only petg and pla) and speed.

So I decided to build my own printer.

Not a Voron.Not a Bambu Lab.Not a Snapmaker.

the printer i wanted didn't existed for my wallet yet so i wanted to  > **Build the best large-format printer I could, using what I already had : parts from my last printer and a lot of time.** 

I designed the mechanics, experimented with different architectures, built custom electronics and firmware configurations, broke things, rebuilt them, measured them, redesigned them, and gradually turned a pile of inexpensive parts into a surprisingly capable machine.

### and One year later...

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
* awd capability (4 motors)
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
---

##  Design philosophy
Whenever possible, I try to use:

* Standard hardware
* Cheap off-the-shelf components
* market knokof
* Reused parts
* Salvaged components
* 3D printed parts
* DIY solutions

The printer is designed to be understood and repaired by its builder.

No proprietary ecosystem should be required to keep the machine running.

### and me and your ar going to Burn thing

Not every idea works.

This will repository intentionally documents prototypes, failed designs, measurements and experiments instead of only showing the final result.


The goal is not simply to assemble existing printer components.
Every part of the machine has been **designed specifically for this project**.

---

#  Documentation

go see the wiki linked in every readme it should explain something if not reach to me

###  Experiments & development
The `Research/` directory contains experiments, prototypes, calculations and design decisions made throughout the development of the printer. i will complete this part in September

---

#  Project status

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



---

#  Why publish the project?

This project started as a personal experiment but i will have to present it to student next year so its a great exercise to put 1 year of thought and dev into simple a git page
The project is also an attempt to document the **engineering process**, not just the final machine.

---

#  Contributing

CR10CORE is primarily a personal project but thanks to my friend who help me at some stage of the project.
Any ideas, improvements, bug reports and discussions are welcome.
If you find a mistake, have an improvement, or simply want to discuss a design choice, feel free to open an Issue or start a Discussion.

---
#  License
This project is open source. and will remain it. any fork should be with the same license

The specific license applying to the CAD files, hardware and software can be found in [`LICENSE`](LICENSE).

---
##  If you like the project
If you find CR10CORE interesting, consider giving the repository a ⭐ on GitHub.


---
