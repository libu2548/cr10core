# Toolhead

The toolhead has gone through several iterations during the development of the printer.
Each version was used to test new ideas, validate mechanisms and solve issues encountered
with previous designs.

---

## V1 — First Version

The first toolhead was mainly focused on validating the general concept.

> A first version designed mostly to look good... but not particularly optimized. 😅

### Features

- Support for stock Creality hotends
- Plotter support
- Large and relatively bulky design

### Issues

- Too heavy
- Poor weight distribution
- No toolboard
- Overall design was not yet optimized for intensive use

---

## V3 — First Major Evolution

The V3 significantly refined the design and introduced several new systems.

### Features

- Support for Bambu Lab hotends
- New cooling system
- Cooling system compatible with RatRig-style turbo fans
- 20 W spindle / laser support

### Issues

- No integrated toolboard
- Not rigid enough around the extruder motor

This version was used to validate several concepts that would later be improved
and integrated into the following versions.

---

## V4 — Current Architecture

The V4 is a more complete evolution of the toolhead, with integrated electronics
and support for several additional tools and sensors.

### Features

- Bambu Lab hotend support
- **BTT EBB42 Gen 2** toolboard support
- Remote turbo fan support
- Spindle / laser support
- **Eddy** sensor support

The main goal of this version is to integrate the different functions required
by the printer while keeping the toolhead as compact and rigid as possible.

---

## V5 — Toolchanger Prototype

The V5 is an experimental version developed to test the concept of a **toolchanger**. could be found on my onshape

Instead of replacing the entire toolhead, the mechanism is designed to change
only the hotend.
because its extreamlyt pricy to have x5 extruder motor x5 tollboard, x5 eddy,x5 fan, x5 cpath turbo fan  (200euros to 300euros)
but we can found esealy for 30/40 euros 5 hotend (snapmake/bambu clone) with heater and temp sensor 
