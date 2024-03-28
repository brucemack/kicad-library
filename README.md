Overview
========

Supplemental symbols/footprints for KiCAD projects.

PCB Checklist
=============

* Keep digital and analog section separate.  Create via fence between sections.
* Use low-pass filter across digital/analog boundary for power/low-speed I/Os.
* Use wider traces (0.5mm) on power traces.
* Double-check capacitor type/ESR on voltage regulators (stability)
* Remember pull-up resistors on I2C traces.
* Don't forget keep-out areas under WIFI antennas, crystal oscillators, etc.
* Update version/date on silkscreen.
* Run DRC on schematic and PCB before completion.
