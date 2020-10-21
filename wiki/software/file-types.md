---
layout: page
title: File types
parent: Software
nav_order: 3
---

# File types

## .gcode

A list of commands that can be processed by the 3D printer firmware.,

This includes movement, heater and generic control commands such as homing, motors off, etc.

Reference:
- [Extensive RepRap G-Code commands list](https://www.reprap.org/wiki/G-code)
- [G-Code commands accepted by Klipper](https://www.klipper3d.org/G-Codes.html)

CNC machines also use G-Code, but have a specialized set of commands that doesn't apply to 3D printers (reference needed).


## .stl, .obj, others

These are common 3D files. Before being sent to the 3D printer, these files need to be [sliced](../slicer/).


## .svg

Scalable Vector Graphic is a format for... 2D vector graphics. They are commonly used by cutters and engravers.

The fact that they're vector-based (as opposed to being raster) means that they include the borders of all the shapes as lines, making computetions for the slicer much simpler.

Graphically speaking vector images can be scaled indefinitely without loss of quality and they can contain precise measurements.

## .photon, .photons

A proprietary file format used by some DLP resin printers from Anycubic. It contains print settings such as layer exposure, bottom exposure, as well as the layer images and commands for the Z axis motor.

