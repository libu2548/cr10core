# CAD Structure

The CR10CORE CAD files are organized by **mechanical assembly** insted of individual part type.

---

## Structure

Each major subsystem of the printer has a folder:

---

#  Assemblies

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
---

#  Version

CAD files may evolve during development.
The current files represent the **latest tested design**
the current test/ prototype design could be found on my onshape : https://cad.onshape.com/documents/71ea23aadc366cfb73b6881e/w/36bb5b319c238c81e5948ca3/e/2af1820cbc9317d82adf2e8e?renderMode=0&uiState=6a86145b25d6108222a77989

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

## Important, Mirrored Parts

Most of the printable parts in this section are provided **without their mirrored counterpart** to avoid duplicating files.

**Remember to print the required parts twice and mirror the second copy in your slicer** when assembling the complete system.
