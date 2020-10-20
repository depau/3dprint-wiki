---
layout: default
title: Stepper drivers
parent: Hardware
nav_order: 2
---

# Stepper drivers

The small controllers called 'stepper drivers' are installed on the motherboard.

This particular controller manages the input current and feeds the output to the motor in the right way; so the driver can manage the full-step and the micro-step of the motor and let it afford the precision usually needed from it.

The most common drivers that can be found on a 3D printer are listed below:


## A4988 (Pololu)

The most common driver, can be found on the majority of chinese kits. Used since the beginning of 3D printing and the RepRap project, it also gave name to the RAMPS board (RepRap Arduino Mega Pololu Shield).

They offer the baseline performance.

## DRV8825

~~You don't want this driver for your printer.~~ [note by Depau: can you explain why?]

Usually more expensive than Pololus, the DRV8825 drivers offer a wider range of microstep capabilities and are allegedly quieter (they're actually not).

## LV8729

This driver may run better than a4988, but worse than a TMC, it is often used for the feeder stepper motor. [Depau: but why do they?]


## Trinamic (TMCxxxx)

This kind of stepper driver is often researched because of the high control and current it can provide to the stepper motor, resulting in precision and torque.

Extra functionality is provided by these drivers, first of all the StealthChop (quiet) mode, supported by all Trinamic drivers.

When used as a drop-in replacement for a Pololu driver, a TMC driver comes with a set of default settings that will mostly work for your printer (you still need to tune the motor current).

However, when configured over UART or SPI, they offer advanced functionality such as sensorless homing (the motor is the endstop) and the StealtChop (quiet) / SpreadCycle (noisier but with higher torque) thresholds.

### TMC2130

Maybe a little outdated, but these were the first Trinamic driver with StallGuard support.

### TMC2208

This driver doesn't support StallGuard, but can support more current tham TMC2130, so more current can be given to the stepper motor, being useful in SpreadCycle mode.

### TMC2209

The last generation of Trinamic drivers: supports StallGuard and SpreadCycle modes.
