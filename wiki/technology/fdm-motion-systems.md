---
layout: page
title: FDM motion systems
parent: Technologies
nav_order: 2
---

# FDM motion systems

**Cartesian _(FDM)_**
Cartesian is a direct, linear relationship between XY motor movement, and toolhead XY motion. Basically, Cartesian movements use individual motors for each axis. Move a single motor (eg, X), and the toolhead moves on the X axis only.

As cartesian is a serial stackup, this can lead to some motors being pushed around by other motors.

A few example of Cartesian motion systems are:
- "i3 style" - This is perhaps the most common enthusiast style Cartesian printer. Usually you'll see these in Prusa i3 (hence the name), Creality CR6/CR10/Ender3 lines. Basically, the bed moves on the Y, while the toolhead controls the X and Z.
- "quadrap/ultimaker style" - This is a box-style printer that often gets confused with CoreXY. A good example of these are Ultimaker printers, or the Creality Ender 5 line. These differ from i3-style printers as the bed often moves on the Z, or not at all, with the toolhead moving on X and Y.

**CoreXY _(FDM)_**
CoreXY uses a parallel manipulator system. In other words, the motors on a CoreXY system are stationary.  In this case, the X and Y motors work together to move along one axis. CoreXY typically has much lower inertia, which allows for more rapid acceleration. The downside is belts are usually twice as long, and harder to tension.


**Delta _(FDM)_**
Delta 3D printers involve a circular print bed with a toolhead featuring three fixed triangular points. Each of these three points can move both upwards and downwards within the cylinder print structure, to be able to place the print head where it needs to be to print.

