
Open drivers for GCC Spirit LS
===============================

The driver for Fabmodules can be found here:
https://github.com/jonnor/fabmodules

Status
--------
- GCC output driver integrated in Fabmodules.
- Basic function present, including upload to printer.
- Can cut/engrave paths with correct proportions.
- PPI, speed and power settings are respected.
- Job offset/origin is respected

TODO (prioritized):

- Fix laser being turned on before the first point (critical)
- Fix output being flipped vertically (workaround: flip input image) 
- Fix/enable relative job origin
- Fix hardcoded scaling factor with correct logic
- Add more workflows in Fabmodules (especially from .svg)
- Add automated tests: .svg/.path -> .gcc
- Document usage/setup
- Upstream the support to fabmodules project

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

