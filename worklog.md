
Monday 1 September 2014
-------------------------

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
