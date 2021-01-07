---
layout: page
title: Devices for OctoPrint
parent: Hardware
nav_order: 2
toc: true
---

# Devices for OctoPrint

In this page is a list of options for running [OctoPrint]({{ '/wiki/software/control-software/#octoprint---' }}) for your printer.

## Easiest option: Raspberry Pi

The Raspberry Pi boards are the easiest option for OctoPrint since the developers provide OctoPi, a Raspberry Pi operating system that runs OctoPrint out of the box.

If you don't know a lot on how to use GNU/Linux and you're not planning to learn, this is your best option.

You need at least a Raspberry Pi 2 for decent performance, and a Raspberry Pi 3 or newer if you also want to run [Klipper]({{ '/wiki/software/firmware/#klipper' }}) or you want Wi-Fi. Make sure you also get a good power supply (your phone's charger is NOT good enough) and an enclosure with cooling, since it tends to get quite hot.

However, if you know how to use Linux or you think you're able to follow the [manual installation guide](https://octoprint.org/download/#installing-manually), get something else.

A list of issues found in Raspberry Pi 2 and 3 (I haven't received a lot of feedback on the Raspberry Pi 4 yet):

- Unless you get a very good SD card, SD cards break fast. Prefer something with different storage types if available.
- The Wi-Fi/Bluetooth module found in the Raspberry Pi 3 is terrible. It randomly crashes, disconnects, drops packets, making Wi-Fi access a lot slower than the maximum supported rate.
- The USB ports in both models often die after a year or two if devices are constantly connected to them.
- The Ethernet in both models is not native. There is in fact a Ethernet to USB 2.0 adatper in the board. Therefore, while they claim it supports 1Gbit speeds, it can only go up to 480Mbps (most realistically ~300Mbps)
- Even if you get a good power supply, you will still likely run into power issues and the power supply won't be able to provide enough power for the whole board and the connected devices.
- The SoC (the CPU, basically) on the Raspberry Pi 3 tends to get extremely hot very fast, so if you don't provide proper cooling, it will constantly throttle at 70°C.

## Recycle old hardware: NUC / old laptop / old desktop

If you have old hardware laying around collecting dust, you can bring it back to life and use it as an OctoPrint machine.

The biggest issue with this approach is the power usage. Older devices won't draw less than 20W of power even while idle, while an ARM single board computer will often draw less than 5W.

You save money on the hardware, but you're gonna spend a lot more in electricity, depending on the rates in your area.

Otherwise pretty much all hardware manufactured after 2008 will easily run both OctoPrint and Klipper at the same time, even Intel Atom-based netbooks (though it might be a bit slow).

I suggest you install Ubuntu Server, Debian or Fedora Server (all free and open-source Linux distrubutions) on them, then install everything else you need. Do me a favor and do not use Windows or macOS: they notoriously use a lot more power than a bare-bones Linux server OS and you'll spend even more in electricity. Also, while OctoPrint runs on all major OSs, if you also want to use Klipper it only runs on Linux.

## Best choice: Other ARM single board computers

There are boards similar to the Raspberry Pi that have comparable advantages (small, cheap, won't double your electicity bill) despite not having the issues.

However, unlike the Raspberry Pi, there are no pre-made operating systems with OctoPrint preinstalled, so you need to do it yourself (don't worry, it's easy).

Here is a (not extensive) list of some of the available options:

- [Orange Pi 4](http://www.orangepi.org/Orange%20Pi%204/) - best board in 2020 (@depau's opinion)
  - Suggested option: $75 with power supply, 4GB RAM and 16GB integrated flash storage, passively cooled aluminum case, cheaper options available
  - Other cases are available online at $10 or less, with heatsinks and a fan
  - It also supports the SD card and there's a cheaper SD card-only model without internal storage
  - Built-in Wi-Fi, Bluetooth, gigabit Ethernet and 2 USB 3.0 ports (one is Type-C)

- [Rock64](https://www.pine64.org/devices/single-board-computers/rock64/)
  - Suggested option: $45 with 4GB of RAM, cheaper options available
  - Power adapter needs to be purchased separately, $7
  - It works with the SD card but you can also buy a 16GB flash storage module for $16
  - It runs very well even without additional cooling
  - It has no Wi-Fi/Bluetooth, it only has gigabit Ethernet
  - One USB 3.0 port

- [RockPro64](https://www.pine64.org/rockpro64/)
  - More expensive and with the same hardware as the Orange Pi 4
  - Suggested option: $80 with 4GB of RAM
  - Power adapter needs to be purchased separately, $7
  - It works with the SD card but you can also buy a 16GB flash storage module for $16
  - You absolutely need a case with a fan and a heatsink
  - Wi-Fi+Bluetooth adapter needs to be purchased separately

If you know other good SBCs, please contribute other options. Make sure they are:

- Stable
- Provide a good power supply
- If they need cooling, please state that
- Powerful enough to run both OctoPrint and Klipper at the same time
- Not a scam
