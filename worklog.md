
Monday 1 September 2014
-------------------------

Done

* Set up and print a test pieces using existing driver from Adobe Illustrator
* Connect machine to Linux, see what device it shows up as. [/dev/usb/lp0](./data/udevinfo.txt)

* Attempted to send .uni file directly to /dev/usb/lp0 using cat. No go, shows empty file on

* Attempt to set up the laser with CUPS
Shows up as "GCC EXPLORER"
Used Generic driver settings, PCL 5.0. Set name to "laser" (expected by fabmodules)
Used defaults for settings, except used manual area and set scaling to "crop".

Attempting to send an .uni file (produced with fabmodules) resulted in no activity

Attempting to send an .epi file results in a job/file showing  up "01" (no name)
``lpr -P laser testfiles/fab_mod_top_layer_crop.epi ``
Job started but showed PCL command error, then HPGL command error.
After 10 seconds the head moved but the laser was seemingly not fireing



TODO:

* Test fabmodules with existing driver+printer.
Not possible, requires Universal or Epilog access?
* Copy universal driver as is
* Attempt to send .uni to printer?
* Modify driver according to spec
* Test

* Video of a first cutting job
* Add end-to-end automated tests.
Input=dxf file, output=.gcc.
Initially Simple geometric shapes
