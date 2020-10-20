---
layout: default
title: Motherboard
parent: Hardware
nav_order: 2
---

# Motherboard

the microcontroller and the stepper drivers are installed on this small board: they can communicate through the firmware.
It is needed to translate the commands listed in a '.gcode' file into movements


## drivers

The small controllers called 'stepper drivers' are installed on the motherboard.
This particular controller manages the input current and feeds the output to the motor in the right way; so the driver can manage the full-step and the micro-step of the motor and let it afford the precision usually needed from it.

The most common drivers that can be found on a 3D printer are listed below:


*A4988:*
the most common driver, can be found on the majority of chinese kits.


*DRV8825:*
you don't want this driver for your printer.

*LV8729:*
this driver may run better than a4988, but worse than a TMC, it is often used for the feeder stepper motor.


**Trinamic**

This kind of stepper driver is often researched because of the high control and current it can provide to the stepper motor, resulting in precision and torque.
Extra functions are provided by this drivers, first of all the stealthchop mode, supported by all Trinamic drivers.
They usually provide the possibility to be installed in multiple ways, such as UART or SPI (*note:* these configurations are required for extra functions, although also in standalone mode, this kind of driver can already work better than a A4988)

*TMC2130:*
maybe a little outdated, but these were the first trinamic driver with stallguard support.

*TMC2208:*
this driver doesn't support stallguard, but can support more current tham TMC2130, so more current can be given to the stepper motor, being useful in spreadcycle mode.

*TMC 2209:*
the last generation of Trinamic drivers: supports stallguard and spreadcycle mode.
