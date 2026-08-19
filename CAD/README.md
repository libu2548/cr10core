# CAD Structure

The CR10CORE CAD files are organized by **mechanical assembly** insted of individual part type.

The goal is to make the CAD easy to understand, modify and reuse without having to open the complete printer assembly first.

---

## 📁 Structure

Each major subsystem of the printer has its own directory:

```text
CAD/
│
├── Toolhead/
│   ├── Parts/
│   ├── Assembly.step
│   ├── Assembly.png
│   └── README.md
│
├── Bed/
│   ├── Parts/
│   ├── Assembly.step
│   ├── Assembly.png
│   └── README.md
│
├── Motion_System/
│   ├── Parts/
│   ├── Assembly.step
│   ├── Assembly.png
│   └── README.md
│
├── Electronics_Bay/
│   ├── Parts/
│   ├── Assembly.step
│   ├── Assembly.png
│   └── README.md
│
└── Enclosure/
    ├── Parts/
    ├── Assembly.step
    ├── Assembly.png
    └── README.md
```

---

# 🧩 Assemblies

Each folder represents a complete subsystem of the printer.

For example:

```text
Toolhead/
│
├── Parts/
│   ├── Toolhead_Main.step
│   ├── Fan_Duct.step
│   ├── Extruder_Mount.step
│   └── ...
│
├── Assembly.step
├── Assembly.png
└── README.md
```

### `Parts/`

Contains the individual components used to build the subsystem.

The files are provided primarily in **STEP format** so that they can be opened and edited in most CAD software.

### `Assembly.step`

Contains the complete assembled subsystem.

This makes it possible to inspect the design without having to manually assemble all the individual components.

### `Assembly.png`

A preview image of the current assembly.

The image is intended to provide a quick visual reference before opening the CAD files.

### `README.md`

A short description of the subsystem and a record of the latest changes.

---

#  Versioning

CAD files may evolve during development.

The current files represent the **latest tested design**, while major changes are documented in the corresponding subsystem README and project changelog.

the current test/ protorype design could be found on my onshape : https://cad.onshape.com/documents/71ea23aadc366cfb73b6881e/w/36bb5b319c238c81e5948ca3/e/2af1820cbc9317d82adf2e8e?renderMode=0&uiState=6a86145b25d6108222a77989

---

#  File formats

The primary CAD exchange format is:

**STEP (`.step`)**

Additional formats may be provided when useful for manufacturing:

* STL 3D printing
* DXF laser cutting / 2D manufacturing
* PDF technical drawings

STEP files should generally be considered the **source CAD geometry**, while STL and other manufacturing files are derived from them.

do not open stl on your desig software to modify them only .step

---
