---
layout: page
title: Environment 🌱
nav_order: 3
toc: true
---

# 3D printing and the environment

This page aims to collect information on how to make sure you handle correctly your 3D printer waste.

If you can, please email your local recycling company and ask them how to dispose of your 3D printer waste.
Report in our Telegram group and/or send a pull-request to the wiki.

{:.no_toc}
## Important note

Always check with your recycling company before disposing of 3D printer waste. Recycling plants are different
and they use different technologies.

## FDM materials

### PETG

In the CONAI (Italian national packing material consortium) 2018
[report](https://docplayer.it/storage/102/153381455/1610022623/KVvuJO_LYdykNXz8O2HI5g/153381455.pdf) (in Italian)
of the "General program of prevention and management of packing materials and packing material waste",
PETG is listed within "not-selectable/recyclable packaging materials with the current state of technology".

This suggests that PETG is **in general** not recyclable with plastic.

#### Milan, Italy (AMSA S.p.A.)

After inquiry, they reported that 3D printer PETG scraps can be disposed of together with plastic waste.

> [...]
> 
> i filamenti in PETG possono essere conferiti nel sacco della plastica
> 
> [...]

### PLA

While PLA is "technically" bio-plastic and it is compostable, this does not imply that all the additives are also
recyclable.

Furthermore, bio materials recycling facilities work differently and use different technologies to speed up the
natural biodegradation, so as always check with your local company.

#### Milan, Italy (AMSA S.p.A.)

After inquiry, they reported that 3D printer PLA scraps should be disposed of with organic waste.

> [...]
>
> i residui derivanti da stampe 3D in materiale PLA (acido polilattico, ossia bioplastica ottenuta da scarti di mais)
> possono essere conferiti nel cassonetto dell'umido. 


### ABS

ABS is technically recyclable. However, recycling companies may or may not be able to separate it from the other types of
plastic. Therefore, you should check with your local company first before disposing of it.

#### Milan, Italy (AMSA S.p.A.)

After inquiry, they reported that 3D printer ABS scraps must be disposed of together with non-recyclable waste:

> [...]
>
> al contrario, quelli in ABS vanno smaltiti nel sacco dell'indifferenziato.


## DLP/SLA UV resins

### Important note

UV resins are often **highly toxic and dangerous for the environment, also potentially carcinogen** in their liquid form.

Make sure you don't rinse off any liquid resin in the sink or in the environment.

Before disposing of resin residues, make sure they're fully cured: use a UV lamp or leave them under the sun for a few days
(but make sure they don't fly away with the wind).

The alcohol used for cleaning can be cured with a UV lamp and then reused. Tests by @Depau showed that both Elegoo's curing (Mercury) 
and wash&cure (Mercury Pro) machines aren't powerful enough for it though. Other curing machines were not tested (I got the damn lamp).

Cure it for a few minutes until it becomes white, stir and cure again, repeat until you see no difference after curing, then do it
one last time. The residue will slowly drop to the bottom over a day and the remaining alcohol can be poured out, then filtered.
The rest can be dried and disposed of.

----

UV resins are thermoset and they are therefore generally not recyclable. Dispose of them with non-recyclable waste.

Some bio-resins exist with claim to be biodegradable, though they often do not specify whether they're also compostable
(you can't just assume they are; many materials are "technically" biodegradable, but they degrade in amounts of time that
are too long for recycling facilities).

Investigation is ongoing with popular bio-resin sellers on the time of decomposition of their products.

#### Milan, Italy (AMSA S.p.A.)

After inquiry, the company reported that DLP/SLA UV resins must be disposed of as such:

- Solid, fully cured resin (in small amounts): non-recyclable bin
- Liquid, uncured resin: it can be brought to one of their "ricicleria" centers in the original container. They will take care of
  it based on the toxycity level ("T" or "F") reported on the label

> I residui di stampa in DLP e SLA, se in piccole quantità, possono essere smaltiti nel sacco dell'indifferenziato.
>
> Se la resina è ancora allo stato liquido, in ricicleria è possibile smaltire rifiuti e prodotti etichettati “T” e/o
> “F” nei loro contenitori originali dove si evidenziano i simboli di tossicità o pericolosità.


## Energy

Even if you can afford a higher electricity bill, using more energy than needed is totally unnecessary and avoidable.

When possible, avoid using particularly old laptops or desktop computers as always-on OctoPrint machines, they use quite a lot
of power and may cost extra 50€/year or more on your bill.

If you want something that stays always-on, consider using a recent (> 2015) laptop or an ARM single-board computer. Or simply
turn everything off when you're not using it. (see: [Devices for OctoPrint]({{ '/wiki/hardware/octoprint-devices/' | absolute_url }}))

Avoid leaving the heated bed on when not needed, and if you can invest on an enclosure, get one: you'll have a better time
printing materials like ABS and you will reduce the amount of energy dissipated as heat in your room.
