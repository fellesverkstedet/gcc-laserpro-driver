
Open drivers for GCC Spirit LS
===============================

The driver for Fabmodules can be found here:
https://github.com/jonnor/fabmodules

Status
--------
- GCC output driver integrated in Fabmodules, can import SVG and PNG.
- Basic vector functionality present, including upload to printer.
- Can cut/engrave paths with correct proportions.
- PPI, speed and power settings are respected.
- Job offset/origin is respected, interpreted from top-left

TODO (prioritized):

- Enable using offset relative to other positions than top-left
- Fix/enable relative job origin
- Add automated tests: .svg/.path -> .gcc
- Document usage/setup
- Upstream the support to fabmodules project
- Send code to Fablab Amsterdam for testing

Later/maybe:

- Implement native raster support
- Integrate support in Lasersaur app


Worklog
--------
[./worklog.md](worklog.md)

Related
----------------

* Near-full set of [GCC LaserPro commands]
(http://www.wiki.cl.cam.ac.uk/rowiki/CompArch/HardwareLab/LaserCutter) (reverse-engineered)

