# CR10CORE

### Homemade large-format CoreXY 3D printer

> A fully custom, large-format CoreXY 3D printer, designed and built from scratch with one main constraint: **make it as good as possible, for as little money as possible.**

![CR10CORE](Documentation/images/cr10core.jpg)

---

## 📖 The story

This is the project that occupied **almost every evening of my 2025–2026 year... and quite a few evenings before and after that.**

In 2025, I was an engineering student who had just failed my first year of preparatory studies. I was broke, but I had a 3D printer: a **Creality CR-10S Pro V2**.

It was already a fairly large printer compared to something like an Ender 3, but I quickly started running into its limitations:

* 🐌 Limited printing speed
* 🛏️ Bed leveling issues
* 🌡️ Warping
* ⚙️ Heavy moving bed
* 🔧 A mechanical architecture that made high-speed printing difficult

So I decided to build my own printer.

Not a Voron.

Not a Bambu Lab.

Not a Snapmaker.

And definitely not an expensive commercial machine.

The goal was much simpler:

> **Build the best large-format printer I could, using what I already had, cheap components, salvaged parts and a lot of engineering.**

What started as a way to get around the limitations of my CR-10S Pro V2 slowly turned into a much bigger project.

I designed the mechanics, experimented with different architectures, built custom electronics and firmware configurations, broke things, rebuilt them, measured them, redesigned them, and gradually turned a pile of inexpensive parts into a surprisingly capable machine.

And then something happened that I absolutely did not expect.

### One year later...

I presented the printer at the **Polytech3D Challenge**.

The machine ended up winning a prize and, more importantly to me, received recognition from several professionals in the 3D printing industry who were present at the event.

A project that started because I couldn't afford the printer I wanted had become a machine I was proud to put in front of people who actually work in the industry.

**This repository is the story of how it happened.**

---

# 🖨️ About the CR10CORE

CR10CORE is a **homemade large-format CoreXY 3D printer** designed around the idea that high performance does not necessarily require expensive hardware.

The machine is built around:

* CoreXY kinematics
* Large build volume
* Klipper firmware
* Custom mechanical components
* Custom electronics integration
* High-speed motion
* Automatic bed leveling
* Input Shaper
* Pressure Advance
* Custom toolhead system
* [Add other confirmed features here]

The project intentionally prioritizes:

**Performance / Cost / Repairability / Modifiability**

rather than following a predefined commercial ecosystem.

---

## 🎯 Design philosophy

The project started with a few simple rules.

### 💰 Keep the cost low

Every expensive component should have a reason to exist.

Whenever possible, I try to use:

* Standard hardware
* Cheap off-the-shelf components
* Reused parts
* Salvaged components
* 3D printed parts
* DIY solutions

### 🔧 Make it repairable

The printer is designed to be understood and repaired by its builder.

No proprietary ecosystem should be required to keep the machine running.

### 🧪 Experiment

Not every idea works.

This repository intentionally documents prototypes, failed designs, measurements and experiments instead of only showing the final result.

### 📐 Design rather than assemble

The goal is not simply to assemble existing printer components.

A large part of the machine has been **designed specifically for this project**.

---

# 📊 Specifications

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

# 📚 Documentation

The documentation is being built alongside the machine.

### 🏗️ Building the printer

* [Getting Started](Documentation/GettingStarted.md)
* [Bill of Materials](Hardware/BOM/BOM.csv)
* [Mechanical Assembly](...)
* [Electronics](...)
* [Wiring](...)
* [Klipper Setup](...)
* [Calibration](...)

### ⚙️ Technical documentation

* [Mechanical design](...)
* [Electronics architecture](...)
* [Firmware](...)
* [Toolchanger](...)
* [Calibration & testing](...)

### 🧪 Experiments & development

The `Research/` directory contains experiments, prototypes, calculations and design decisions made throughout the development of the printer.

---

# 🗺️ Project status

The CR10CORE is an evolving project.

| Subsystem     | Status            |
| ------------- | ----------------- |
| Frame         | 🟢 Functional     |
| CoreXY motion | 🟢 Functional     |
| Z axis        | 🟢 Functional     |
| Extrusion     | 🟢 Functional     |
| Electronics   | 🟢 Functional     |
| Klipper       | 🟢 Functional     |
| Input Shaper  | 🟢 Tuned          |
| Bed leveling  | 🟢 Functional     |
| Toolchanger   | 🟡 In development |
| Documentation | 🟡 In progress    |

> The status above will evolve as the project continues.

---

# 📸 Gallery

<!-- Add photos and videos of the printer here -->

---

# 🧠 Why publish the project?

This project started as a personal experiment.

I am publishing it because I want the work, experiments and solutions developed during the project to be useful to other makers.

If someone can take one of the ideas from this project, improve it, build their own machine or simply understand something better because of this repository, then publishing it was worth it.

The project is also an attempt to document the **engineering process**, not just the final machine.

---

# 🤝 Contributing

CR10CORE is primarily a personal project, but ideas, improvements, bug reports and discussions are welcome.

If you find a mistake, have an improvement, or simply want to discuss a design choice, feel free to open an Issue or start a Discussion.

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for more information.

---

# 📜 License

This project is open source.

The specific license applying to the CAD files, hardware and software can be found in [`LICENSE`](LICENSE).

---

## ⭐ If you like the project

If you find CR10CORE interesting, consider giving the repository a ⭐ on GitHub.

It helps the project get noticed and motivates me to keep documenting it.

---

**CR10CORE — Built because I couldn't afford the printer I wanted.**
