Overview
========

Supplemental symbols/footprints for KiCAD projects.

PCB Quality Checklist
=====================

* Use 3.5mm mounting holes. Center of hole should be 4mm from edge of board.
* Include test points on critical nets. Use 1.5mm x 1.5mm footprints.
* Double-check capacitor type/ESR on voltage regulators (stability)
* Double-check transformer pin mappings between schematic and footprint, these 
can be tricky.  Make sure the windings are connected as expected.
* Remember pull-up resistors on I2C traces (not needed for Pico)
* Pay attention to phasing marks on bifilar/trifilar RF transformers. Make
sure that the footprint matches the schematic.
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
* SMA connectors (AMP 901-144)

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
* Flood signal layers with GND for added shielding.

JLCPCB BOM File
===============

Create a property called "LCSC" and put the LCSC part number in for each component.

Use the "Exclude from BOM" checkbox to designate parts that shouldn't be populated onto the board. NOTE: You also need to uncheck the "Show 'Exclude from BOM'" box in the BOM export dialog to remove these components from the finished BOM file.

The standard KiCAD BOM file export feature can be used, however unnecessary columns should 
be deleted and others need to be renamed. Required column names are:

        Designator	Comment	JLCPCB Part#(optional)	Footprint

JLCPCB CPL File
===============

In the PCB editor, go to File ... Fabrication Output ... .POS file.

Select CSV, millimeters, exclude components with DNP

The following changes are required:

    Ref to Designator 
    PosX to Mid X 
    PosY to Mid Y 
    Rot to Rotation 
    Side to Layer

So columns are:

        Designator	Val	Package	Mid X	Mid Y	Rotation	Layer


