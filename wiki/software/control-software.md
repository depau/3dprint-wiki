---
layout: default
title: Control software
parent: Software
nav_order: 3
---

# Control software

While many printers can work completely independently by reading [G-Code files]({{ '/wiki/software/file-types/#gcode' | absolute_url }}), most FDM printers also have a USB port that can be used to control them and run prints.


## OctoPrint <i class="fa fa-linux" aria-hidden="true"></i> <i class="fa fa-apple" aria-hidden="true"></i> <i class="fa fa-windows" aria-hidden="true"></i>

*License: open-source, GNU AGPL v3.0*

OctoPrint is the most widely used control software for FDM 3D printers. It shows a web-based interface, it allows you to start, control and monitor prints.

It can also integrate with MJPEG-Streamer or with uStreamer to stream a video of the printer if you add a webcam to it.

OctoPrint also provides pre-installed OctoPi images for Raspberry Pi boards

[https://octoprint.org](https://octoprint.org)


## Repetier Host <i class="fa fa-linux" aria-hidden="true"></i> <i class="fa fa-apple" aria-hidden="true"></i> <i class="fa fa-windows" aria-hidden="true"></i>

*License:*
- *up to version 0.91: open-source, Apache 2*
- *after version 0.91: proprietary, closed-source*

Repetier-Host is a control software for FDM printers and despite what the name might suggest, it works with most firmwares, including Marlin, though it supports more features when the printer is running Repetier-Firmware.

It has integrated slicing support using Slic3r or Cura, and it features toolpath preview and full printer control.

Unlike OctoPrint it is not intended to be used on headless machines or Single Board Computers, it runs on a regular computer which needs to stay on all the time while the printer is running.

