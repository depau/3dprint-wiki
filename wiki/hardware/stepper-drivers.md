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


## Trinamic-based (TMCxxxx)

This kind of stepper driver is often researched because of the high control and current it can provide to the stepper motor, resulting in precision and torque.

Extra proprietary functionality is provided by these drivers, but not all of them support all features.

Here is a translation from "sales people English" to "normal people English" for the most common Trinamic features:

- StealtChop: "Quiet mode", the motors run extremely quietly at low-ish speeds, while still providing very good torque.
- SpreadCycle: "Noisier mode", the motors are noisier but they provide higher torque. Usually appropriate for higher speeds to prevent skipping steps.
- StallGuard: Motor stall detection (sensorless homing). The driver can act as an endstop by pulling a pin low when a stall is detected. It needs tuning.
- CoolStep: The motor current is adjusted dynamically based on feedback from the "StallGuard" circuitry, allowing cooler motor operation when the motor requires less torque.
- MicroPlyer: Fancy name for their proprietary micro-stepping circuitry.

Some drivers are allegedly resistant to shorts, in case you happen to work with screwdrivers nearby while your hands are shaking.

The parameters for the features above can be configured using the additional UART, SPI or I²C configuration protocol (depending on the driver model).
For example, you can tune the speed threshold at which the driver goes from StealtChop to SpreadCycle, as well as minimum/maximum current values for each mode (CoolStep)

When used as a drop-in replacement for a Pololu driver, a TMC driver comes with a set of default thresholds that will mostly work for most printers. A trim-potentiometer is also provided like in regular steppers, and if enabled in the driver settings (it's usually enabled out of the box), the current can be tuned with the classic ceramic screwdriver.

However, when configured over UART or SPI, they offer advanced functionality. The trim-port can also be disabled in order to tune the current more precisely, programmatically.

UART/SPI configuration is usually performed externally with additional hardware and software. However, some  boards like the SKR 1.3 and 1.4 have the internal wiring to allow for configuration through the firmware.

The STALL pin (for StallGuard/sensorless homing) is also internally connected to the respective endstop pin. This is why the board manual suggests to clip it off if you're not planning to use the feature.

### TMC2130

Maybe a little outdated, but these were the first Trinamic driver with StallGuard support.

- SPI configuration
- StealtChop
- SpreadCycle
- StallGuard / Stall detection / Sensorless homing
- Phase current: 1.2A (QFN36 package), 1.4A (eTQFP48 package)
- Motor supply: 4.75V to 46V
- Snallest microstep: 1/256

### TMC2208

This driver doesn't support StallGuard, but can support more current tham TMC2130, so more current can be given to the stepper motor, being useful in SpreadCycle mode.

- UART configuration
- StealtChop
- SpreadCycle
- ~~StallGuard~~ not supported
- MicroPlyer
- Phase current: 1.4A
- Motor supply: 4.75V to 36V
- Snallest microstep: 1/256

### TMC2209

The last generation of Trinamic drivers: supports StallGuard and SpreadCycle modes.

- UART configuration
- StallGuard / Stall detection / Sensorless homing
- StealtChop
- SpreadCycle
- MicroPlyer
- Phase current: 2.0A
- Motor supply: 4.75V to 29V
- Snallest microstep: 1/256
