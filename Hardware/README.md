# Hardware

This section explains the main hardware choices made for the printer and the reasons behind them.

## Mainboard — BTT Octopus Pro

The printer uses a **BTT Octopus Pro** as its main controller.

The main reason for choosing this board was its large number of available stepper driver slots and I/O, which makes it well suited for a complex CoreXY printer with multiple independent Z motors and additional tools.

Another important advantage is that the Octopus Pro can support **higher-voltage configurations**, making it possible to move to a **48 V system in the future** if needed.

For this project, the printer is currently running at 24 V, but the choice of the Octopus Pro leaves room for future upgrades without having to completely redesign the electronics.

---

## Stepper Drivers — TMC2209

The printer uses **TMC2209** stepper drivers.

They were mainly chosen because they are:

## VERY CHEAP

---

## AWD CoreXY

The printer uses an **AWD (All-Wheel Drive) CoreXY** configuration.

Instead of using only two motors for the XY motion, the system uses **four independent motors**, with two motors driving each axis.

i use this beacose in a traditional corexy there is a verry long belt beetween the motor and carriage (1m) introducing a spring like vibration, so by uting 2 in diagonal we can shorten the lengt beetwin the carriage from 1m to 50cm)

The four motors are controlled independently.

This configuration requires four stepper drivers instead of the two normally required for a standard CoreXY.

---

## 3-Point Z Tilt

The bed is mounted on **three independent Z motors**.

Each motor controls one point of the bed, allowing the firmware to independently adjust the three points and compensate for small differences in the bed or frame geometry.

This is used with **Z-Tilt** in Klipper.

The three-point configuration was chosen because three points naturally define a plane. This makes it possible to level the bed mechanically by adjusting the position of each corner independently, without requiring the bed itself to be perfectly aligned with the frame.

The system therefore uses three additional stepper drivers, bringing the total required for the motion system to **seven drivers**:

* 4 × XY motors for AWD CoreXY
* 3 × Z motors for Z-Tilt

---

## Toolboard

A **toolboard** is mounted directly on the toolhead.

The main purpose is to move as much of the toolhead electronics as possible away from the main electronics panel.

Instead of running individual cables for every component all the way back to the mainboard, the toolboard handles the local connections for things such as:

* Hotend
* Fans
* Temperature sensors
* Eddy sensor
* Other toolhead peripherals

This significantly reduces the number of cables running through the moving cable chain.

It also makes the toolhead easier to modify or service, since most of its electronics are concentrated in one location.

The current design uses a **BTT EBB42 Gen 2** toolboard connected to the main controller through **CAN bus**.
