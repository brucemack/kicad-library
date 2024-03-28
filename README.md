Overview
========

Supplemental symbols/footprints for KiCAD projects.

PCB Checklist
=============

* Keep digital and analog section separate.  Create via fence between sections.
* Use low-pass filter across digital/analog boundary for power/low-speed I/Os.
* Via fence around sensitive traces.
* Use wider traces (0.5mm) on power traces.
* Double-check capacitor type/ESR on voltage regulators (stability)
* Remember pull-up resistors on I2C traces.
* Don't forget keep-out areas under WIFI antennas, crystal oscillators, etc.
* Update version/date on silkscreen.
* Run DRC on schematic and PCB before completion.
* Review all schematic pages to make sure there are no warning notes or TODOs left
from the schematic phase.
* Make PDF of schematic that matches the files sent to the fab.
* Double-check to make sure all files are committed to version control.
* Place order for components needed to build board.

