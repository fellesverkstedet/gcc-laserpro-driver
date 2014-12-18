
1. Install GNU/Linux
-----------------------

Any dekstop GNU/Linux system should work.
[Ubuntu 14.04 LTS](http://releases.ubuntu.com/14.04/) has been tested and is recommended.
The rest of the instructions might need some changes if using another distribution.

2. Setup CUPS printer service
-------------------------

Open a web browser, go to http://localhost:631

If this does not give you a web interface make sure CUPS is intalled, and that cupsd is running.

    Go to Adding new Printers -> Add Printer
    Select your printer, should be "GCC EXPLORER" or similar
    Continue
    (very important) Give it the Name: laser
    Continue
    Chose Make: Generic
    Continue
    Chose Model: Generic PCL 5 LF Printer - CUPS+GutenPrint
    Add Printer
    Chose Media Size: Manual
    Chose Shrink Page: Crop
    Set Default Options

It should now say setup success, and show the status of the printer as Idle.
    

3. Install fabmodules
-------------------

Right now a custom version of Fabmodules is needed. In the future,
the version should be downloadable at the [regular](http://kokompe.cba.mit.edu/downloads.html) location.

Open a terminal

    Alt + F2 -> type gnome-terminal -> Enter

Install dependencies

    sudo apt-get install python python-wxgtk2.8 python-dev python-pip gcc g++ libpng12-dev libgif-dev make bash okular libboost-thread-dev libboost-system-dev cmake git

Get the code

    git clone https://github.com/fellesverkstedet/fabmodules.git
    cd fabmodules

Build & install

    make fab
    sudo make install

4. Run & Verify install
---------------------

Ensure that your GCC laser cutter is plugged in over USB.

In the terminal

    fab

Choose "Vector SVG" and "GCC laser cutter", hit "Start".
A new window should appear.

Load an SVG file, click "make path", then "make gcc" and then "Send it!"

Your toolpath should now show on your GCC laser control panel,
and if you press "Start" it should cut.

