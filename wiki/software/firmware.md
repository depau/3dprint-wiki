---
layout: page
title: Firmware
parent: Software
nav_order: 3
---

# 3D printer firmware

Here is a list of common firmware for 3D printer main boards.

Check out the [firmware category](https://www.reprap.org/wiki/Category:Firmware) on the [{% include reprap %}](https://www.reprap.org) for a more extensive list.

## Marlin

- License: open-source, GNU GPL v3.0
- Supported hardware:
  - ATmega AVR (Arduino/RAMPS, Teensy, more)
  - ARM Cortex Mx (Arduino Due, STM32, Smoothieboard, SKR)
  - Xtensa (ESP32)
  - Linux

Marlin is the most popular 3D printer firmware. It supports pretty much any feature you might be looking for, and is shipped as stock firmware by 3D printer manufacturers.

[{% include website %}](https://marlinfw.org/) - [{% include reprap %}](https://reprap.org/wiki/Marlin) - [{% include wiki %}](https://en.wikipedia.org/wiki/Marlin_(firmware)) - [{% include github %}](https://github.com/MarlinFirmware/Marlin)


## Repetier-Firmware

- License: open-source, GNU GPL v3.0
- Supported hardware:
  - ATmega AVR (Arduino/RAMPS, Teensy, more)

Repetier is also quite popular and sometimes shipped as stock firmware by manufacturers, however it is becoming less popular since many newer boards ship with more powerful 32-bit ARM microcontrollers.

One of its distinctive features is the web-based configurator, with many presets and very well documented.

It supports FDM 3D printers, laser engravers and CNC machines.

[{% include website %}](https://www.repetier.com/documentation/repetier-firmware/) - [{% include reprap %}](https://reprap.org/wiki/Repetier-Firmware) - [{% include github %}](https://github.com/repetier/Repetier-Firmware)


## Klipper

- License: open-source, GNU GPL v3.0
- Supported hardware:
  - ATmega AVR (Arduino/RAMPS, Teensy, more)
  - ARM Cortex Mx (Arduino Due, STM32, Smoothieboard, SKR)
- Host software:
  - Linux only

Klipper is a pretty unique firmware. It solves the problem of having to perform crazy optimizations to perform fast computations on slow microcontrollers by performing all the computations on a Linux machine.

The 3D printer motherboard firmware is extremely simple, porting it to new hardware is very simple. The firmware is "dumb", it doesn't know how to operate a printer and it is only instructed how to safely shut it down in case of failure.

All movements are precomputed and sent over by its Linux companion, Klippy. Klippy is written in Python, which allows the developer to focus on functionality and stability instead of having to constantly have to work around the microcontroller limitations. Klipper in fact uses proper kinematic equations instead of optimized versions, leveraging the better floating point arithmetic support in Python.

This architecture allows notoriously resource-constrained boards, such as the RAMPS to run at up to 154 steps per second. On top of that, it allows for very simple configuration, advanced movement control and advanced configuration if desired. Klipper provides the best performance on all supported boards.

It also supports more exotic configurations, such as multiple main boards controlling the same printer (for example, multiple Arduino Uno-based mini-RAMPS) and multiple LCD displays.

Fancy features are also supported, such as a proper "pressure advance" algorithm, best in class "look ahead" support (due to in practice no RAM constraints), automatic or computer-assisted calibration for pretty much everything that needs calibration and, when paired with Trinamic drivers, it supports changing the configuration at runtime from OctoPrint, without the need to reflash the firmware.

It deeply integrates with OctoPrint through a plug-in, you can both control the printer with OctoPrint and you can also control OctoPrint with the printer's LCD. The same device that runs Klippy can also run OctoPrint.

[{% include website %}](https://www.klipper3d.org/) - [{% include reprap %}](https://reprap.org/wiki/Klipper) - [{% include github %}](https://github.com/KevinOConnor/klipper/)
