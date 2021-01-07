---
layout: page
title: Slicers
parent: Software
nav_order: 2
toc: true
---

# Slicers

"Slicer" is the generical name for the softwares used to convert a 3D model to a ".gcode" file.

The most common slicers are listed below:

## FDM/FFF
### Ultimaker Cura <i class="fa fa-linux"></i> <i class="fa fa-apple"></i> <i class="fa fa-windows"></i>

*License: open-source, GNU LGPL v3.0*

It has been one of the most common for a long time, because of the control it can provide.

It ships with default configurations for most kits and preassembled printers.

Most slicers now include the same or even more features, while Cura requires a lot more system resources and runs very slow on mid-end computers.

[https://ultimaker.com/software/ultimaker-cura](https://ultimaker.com/software/ultimaker-cura)

### Slic3r <i class="fa fa-linux"></i> <i class="fa fa-apple"></i> <i class="fa fa-windows"></i>

*License: open-source, GNU AGPL v3.0*

Slic3r is the father of a lot of now-more-popular knock-off slicers listed below. While it started with many experimental features, Slic3r is currently one of the most robust and stable slicers in existence.

Maintainers have tough requirements to guard against regressions and bad code quality, which prompted people who want to *live on the edge* to maintain their fork with more experimental features.

On top of being one of the most accurate slicers and (opinion mine) the slicer that produces the best bridges, Slic3r is very fast: the UI is snappy even on slow hardware and the slicing leverages multi-threading where available.

It claims to support DLP/SLA, though in my experience its support is extremely basic and pretty much unusable.

[https://slic3r.org/](https://slic3r.org/)

### Prusa Slicer <i class="fa fa-linux"></i> <i class="fa fa-apple"></i> <i class="fa fa-windows"></i>

*License: open-source, GNU AGPL v3.0 (Slic3r fork)*

Even though it is developed by Prusa Research for their lineup of 3D printers, Prusa Slicer can also be used with other printer manufacturers.

Prusa doesn't list a detailed set of additional features on top of Slic3r: roughly the changes go from a UI revamp to a rewrite of all the Perl code to C++.

It is quite stable and resource usage is comparable to Slic3r.

It supports DLP printers (since Prusa Research also makes DLPs). However, it is not comparable with dedicated DLP slicers.

[https://www.prusa3d.com/prusaslicer/](https://www.prusa3d.com/prusaslicer/)

### SuperSlicer <i class="fa fa-linux"></i> <i class="fa fa-apple"></i> <i class="fa fa-windows"></i>

*License: open-source, GNU AGPL v3.0 (Slic3r fork)*

Yet another Slic3r fork, previously known as Slic3r++, SuperSlicer is a fork of Prusa Slicer, which in turn is a fork of Slic3r.

SuperSlicer includes all improvements made by Prusa, plus a set of additional experimental changes. While it is not resource-intensive, it includes a lot of changes that haven't been properly reviewed/tested. It can be thought of Slic3r but with experimental cool features.

Additional changes include all Prusa Slicer changes + top surface ironing, allegedly better thin walls, overhangs and brims. In my experience it is pretty much usable, albeit having some regressions in the infill code in complex models.

[https://github.com/supermerill/SuperSlicer/](https://github.com/supermerill/SuperSlicer/)

### Simplify3D <i class="fa fa-linux"></i> <i class="fa fa-apple"></i> <i class="fa fa-windows"></i>

*License: proprietary, paid ($149 at the time of writing)*

A good slicer, but (opinion) not worth the price considering the excellent free and open-source alternatives. All other slicers have the same features, the only reason why one would buy it is to get their customer support.

[https://www.simplify3d.com/](https://www.simplify3d.com/)

## DLP

### Slic3r, Prusa Slicer and SuperSlicer <i class="fa fa-linux"></i> <i class="fa fa-apple"></i> <i class="fa fa-windows"></i>

See above. They work best for FDM printers, but they also support DLP/SLA.

### ChituBox <i class="fa fa-linux"></i> <i class="fa fa-apple"></i> <i class="fa fa-windows"></i>

*License: proprietary, freeware (requires signing up to their website to download it)*

This is the most common slicer used for SLA technology. It offers advanced features and settings, presets for many preassembled printers.

[https://www.chitubox.com/](https://www.chitubox.com/)

### Anycubic Photon Workshop <i class="fa fa-windows"></i> (using [Wine](https://www.winehq.org/): <i class="fa fa-linux"></i> <i class="fa fa-apple"></i>)

*License: proprietary, freeware*

Developed by Anycubic for Anycubic products, it is your only option if your printer only accepts the newer Photon S file format which is not supported by ChituBox.

It is an okay slicer, it does its job but it's not the best one out there.

[https://www.anycubic.com/](https://www.anycubic.com/)
