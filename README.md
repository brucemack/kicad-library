Overview
========

Supplemental symbols/footprints for KiCAD projects.

PCB Checklist
=============

* Use 3.5mm mounting holes.
* Include test points on critical nets. Use 1.5mm x 1.5mm footprints.
* Double-check capacitor type/ESR on voltage regulators (stability)
* Remember pull-up resistors on I2C traces.
* Don't forget keep-out areas under WIFI antennas, crystal oscillators, etc.
* Update version/date on schematic and PCB pages in KiCAD.
* Update version/date on silkscreen.
* Review component references to make sure none are blocked (ex: vias).
* Run DRC on schematic and PCB before completion.
* Review all schematic pages to make sure there are no warning notes or TODOs left
from the schematic phase.
* Polarity on tantalum/electrolytic capacitor footprints
* Make PDF of schematic that matches the files sent to the fab.
* Double-check to make sure all files are committed to version control.
* Make sure all dependent symbol/footprint libraries have been committed to version control.
* 1% tolerance on critical voltage dividers
* Place order for components needed to build board.

PCB Layout Rules for Performance
================================

* 4 layer stack-up: Signal, Ground, Power, Signal
* External connections are best placed on board edges.
* Decoupling capacitors should be as close as possible. Use a T-type connection 
to the ground plane using a via (i.e. one end of capacitor overlapping Vcc lead
and other end connected to a ground via).
* Crystals should be located as close as possible.
* Use a single ground-plane with as few breaks as possible.
* Keep digital and analog section separate.  Create via fence between sections.
* Use low-pass filter across digital/analog boundary for power/low-speed I/Os.
* Via fence around sensitive traces.
* Use wider traces (0.5mm) on power traces.
