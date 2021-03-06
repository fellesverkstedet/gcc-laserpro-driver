
Open drivers for GCC Spirit LS
===============================

The driver is integrated in Fabmodules, and can be found here:
https://github.com/fellesverkstedet/fabmodules

Status
--------
Basic functionality working

- GCC output driver integrated in Fabmodules, can import SVG and PNG.
- Basic vector functionality present, including upload to printer.
- Can cut/engrave paths with correct proportions.
- PPI, speed and power settings are respected.
- Job offset/origin is respected, interpreted from top-left

TODO
-----
Prioritized:

- Enable using offset relative to other positions than top-left
- Upstream the support to fabmodules project
- Send code to Fablab Amsterdam for testing


Later/maybe:

- Add automated tests: .svg/.path -> .gcc
- Fix/enable relative job origin
- Implement native raster support
- Integrate support in Lasersaur app

Installing
------------
See [./SETUP.md](SETUP.md)

Demos videos
--------------

[![First complete cut](http://img.youtube.com/vi/T_f-NWOrRFQ/maxresdefault.jpg)](https://www.youtube.com/watch?v=T_f-NWOrRFQ)


Worklog
--------
[./worklog.md](worklog.md)

Related
----------------

* Near-full set of
[GCC LaserPro commands](http://www.wiki.cl.cam.ac.uk/rowiki/CompArch/HardwareLab/LaserCutter) (reverse-engineered)

