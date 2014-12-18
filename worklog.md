

Monday 1 September 2014
-------------------------

Time spent: 9 hours

Set up and print a test pieces using existing driver from Adobe Illustrator
Connect machine to Linux, see what device it shows up as. [/dev/usb/lp0](./data/udevinfo.txt)

Attempted to send .uni file directly to /dev/usb/lp0 using cat. No go, shows empty file on

Attempt to set up the laser with CUPS. 
Shows up as "GCC EXPLORER".
Used Generic driver settings, PCL 5.0. Set name to "laser" (expected by fabmodules).
Used defaults for settings, except used manual area and set scaling to "crop".

Attempting to send an .uni file (produced with fabmodules) resulted in no activity

Attempting to send an .epi file results in a job/file showing  up "01" (no name)
``lpr -P laser testfiles/fab_mod_top_layer_crop.epi ``
Job started but showed PCL command error, then HPGL command error.
After 10 seconds the head moved but the laser was seemingly not fireing

Sending the file from within fabmodules also works as expected.

Added a skeleton GCC driver, based on the exiting one for Epilog

Modified and tweaked the driver to be able to cut paths.

Dumped some output files from existing driver to figure out how pen intensity/speed/ppi was encoded.
Using "FILE" as the port of the Windows printer, as found under Preferences on the printer setup,
was a very easy way to do this.
Turned out to be 4-character 0-padded ascii values, for each of the 16 pens.

Recorded a short video of current status.


Thursdag 4 September 2014
----------------------------

Time spent: 7 hours

Verified origin/offset generally working.

Debugged why laser turns on when sending pen-up (PU) commands.
It seems that when using position-relative (PR), as original driver does, this does not occur.
However, sending a select-pen (SR) command the issue is also avoided. Unclear why.

Fixed the inverted Y axis. Currently assumes 460 mm work-area.
Made a more generic fix for correct proportions, both for job origin and scaling.

Added Fabmodules workflow from SVG to GCC


Thursday 18 December 2014
---------------------------

Time spent: 

Verified existing setup still working.
In Arch Linux, the CUPS service had been renamed from cups.service to org.cups.cupsd.service
Worked when taking this into account.

On Arch Linux, also need to fix Python hashbangs because Python3 is default

    sed -i -e "s|#![ ]*/usr/bin/python$|#!/usr/bin/python2|" -e "s|#![ ]*/usr/bin/env python$|#!/usr/bin/env python2|" bin/*

Remove autofocus button, replaced with "Make sure to focus" text.

Installed Ubuntu 14.04 on laser cutter control machine. Installing to USB stick failed,
using Virtualbox in Windows instead. Documenting process going along so others can reproduce.


