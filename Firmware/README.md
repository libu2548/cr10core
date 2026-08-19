#  Software

The CR10CORE uses **Klipper** as its firmware.

The software architecture is split between a Raspberry Pi, which runs the main software, and diferent slave microcontrollers that directly control the printer's hardware.

---

## 🧠 How does Klipper in my system work?

```text
                    Raspberry Pi
                 ┌──────────────────┐
                 │                  │
                 │     Klipper      │
                 │                  │
                 │  Configuration   │
                 │     Macros       │
                 │    G-code        │
                 │    Planning      │
                 │realtime computing│
                 │                  │
                 └────────┬─────────┘
                          │
                      USB / CAN 
                          │
          ┌───────────────┴───────────────┐
          │                               │
   ┌──────▼──────┐                 ┌──────▼──────┐
   │ Octopus Pro │                 │   EBB42     │    i2c
   │             │                 │    GEN2     │───────────────┐
   │ Main MCU    │                 │  Toolhead   │               │
   └──────┬──────┘                 └──────┬──────┘        ┌──────▼──────┐
          │                               │               │ eddy coil   │ 
      Motors /                         Hotend             └──────┬──────
      heaters /                        Fans                   bed level
      endstops                         Sensors               z endstop
      etc.                             Extruder                 tap
      
      
```

The Raspberry Pi runs the main **Klipper host software** (`klippy`).

The microcontrollers run a small Klipper firmware that receives precise movement and control instructions from the Raspberry Pi.

The Raspberry Pi to handle the high-level logic while the dedicated MCUs handle hardware control.

---

#  Raspberry Pi

The Raspberry Pi is the **brain of the printer**.

It runs:

* Klipper
* Moonraker
* mansail
* Configuration files
* G-code processing
* Macros
* Calibration data

The Raspberry Pi does **not directly drive the stepper motors or heaters**.

Instead, it communicates with the printer's microcontrollers.

For CR10CORE, the main controller is an **Octopus Pro**, with an **EBB42 GEN2** used as a toolhead controller.

---

# Octopus Pro

The **BIGTREETECH Octopus Pro** is the main electronics board of the printer.

It contains an STM32 microcontroller running Klipper firmware.

It is responsible for most of the printer's hardware:

* X/Y/Z stepper motors
* Additional xyz motors
* Heaters
* Fans
* Endstops
* Thermistors
* Other peripherals

The Octopus Pro communicates with the Raspberry Pi through USB.

### Official documentation

[BIGTREETECH Octopus Pro documentation](https://github.com/bigtreetech/BIGTREETECH-OCTOPUS-Pro)

[BIGTREETECH Octopus Pro Wiki](https://github.com/bigtreetech/docs/blob/master/docs/Octopus%20Pro.md)

---

# Toolhead controller : EBB42 GEN2

The **EBB42 GEN2** is a small stm32 board located directly on the toolhead.

Instead of running all of the toolhead wiring of fan extrifer, probe and heater back to the mainboard, the EBB42 handles the components located around the hotend.

For example:

```text
                 EBB42 GEN2
              ┌───────────────┐
              │               │
              │ STM32G0B1     │
              │               │
              └───────┬───────┘
                      │
        ┌─────────────┼──────────────┐
        │             │              │
     Extruder       Hotend         Fans
     motor         heater
                    │
                 Thermistor
```

Depending on the configuration, the EBB42 can also handle:

* Extruder motor
* Hotend heater
* Thermistors
* Fans
* Probe
* ADXL345
* Eddy Coil
* Other toolhead sensors

The EBB42 GEN2 can communicate with the Raspberry Pi through **USB or CAN**. The CR10CORE configuration can use whichever interface is selected in the machine configuration.

The EBB42 GEN2 uses an **STM32G0B1** microcontroller.

### Official documentation

[BIGTREETECH EBB42 GEN2 documentation](https://github.com/bigtreetech/docs/blob/master/docs/EBB42_GEN2.md)

[BIGTREETECH EBB firmware and configuration files](https://github.com/bigtreetech/EBB)

---

# Eddy Coil

The **Eddy Coil** is a non-contact inductive sensor used by the CR10CORE for bed probing and mesh calibration.

differentry from a traditional mechanical probe, it does not need to physically touch the bed.

The sensor works by detecting changes in an electromagnetic field caused by the surface underneath it.

and ecipecally it doesent act like an trigger edndstop it can give the heigt at any time or z level with an command

The Eddy Coil connects to the toolhead electronics through **I²C**.

In the CR10CORE:

```text
Raspberry Pi
     │
     │ USB
     ▼
  EBB42 GEN2
     │
     │ I²C
     ▼
 Eddy Coil
     │
     ▼
     Bed
```

The official documentation recommends mounting the Eddy sensor approximately **2–3 mm above the bed when the nozzle is touching the bed**. The exact installation and calibration procedure should always follow the sensor documentation.

### Official documentation

[BIGTREETECH Eddy documentation](https://github.com/bigtreetech/docs/blob/master/docs/Eddy.md)

[BIGTREETECH Eddy GitHub repository](https://github.com/bigtreetech/Eddy)

### unofficial documentation of eddy ng
we are gonna use a user modified version of eddy introducing some fix and added features like eddy tap.

https://github.com/vvuk/eddy-ng

https://github.com/vvuk/eddy-ng/wiki

---

# 🖥️ Klipper software stack

The complete software stack looks like this:

```text
                         Web browser
                              │
                              ▼
                           mansail
                              │
                              ▼
                         Moonraker
                              │
                              ▼
                           Klipper
                          (klippy)
                              │
                ┌─────────────┴─────────────┐
                │                           │
               USB                         USB
                │                           │
                ▼                           ▼
         Octopus Pro                    EBB42 GEN2
         Main MCU                       Toolhead MCU
                                            │
                                            ▼
                                        Eddy Coil
```

### mansail

mansail is the web interface used to control the printer.

It provides:

* Printer control
* G-code upload
* Temperature monitoring
* Console
* Configuration editing
* Graphs
* Print management

### Moonraker

Moonraker is an API server that sits between mansail and Klipper.

It allows the web interface and other applications to communicate with Klipper.

---

# 📁 Configuration

The main configuration file is:

```text
printer.cfg
```

Additional configuration files can be included using:

```ini
[include filename.cfg]
```

This allows the configuration to be split into logical components.

For example:

```text
config/
│
├── printer.cfg
├── steppers.cfg
├── extruder.cfg
├── toolhead.cfg
├── eddy.cfg
├── macros.cfg
└── calibration.cfg
```

This is particularly useful for CR10CORE because the machine has a relatively complex hardware architecture.

---

#  Official Klipper documentation

For detailed information about Klipper itself, always refer to the official documentation:

[Klipper Documentation](https://www.klipper3d.org/ )

[Klipper Configuration Reference](https://www.klipper3d.org/Config_Reference.html )

[Klipper Installation](https://www.klipper3d.org/Installation.html )

[Klipper Overview](https://www.klipper3d.org/Overview.html )

---

# ⚠️ CR10CORE configuration

The files used by the actual CR10CORE configuration are available in:

```text
Firmware/
└── Klipper/
    ├── printer.cfg
    ├── macros/
    └── boards/
```

The configuration found in this repository represents the configuration of **my specific machine**.

It should therefore **not be copied blindly to another printer**.

Hardware revisions, pin assignments, MCU IDs, thermistors, motors and mechanical dimensions may differ.

When building your own CR10CORE or using parts of this project, always verify the relevant configuration against the official hardware documentation.

