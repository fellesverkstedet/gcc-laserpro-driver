Instructions specific to [Fellesverkstedet](http://fellesverkstedet.no) setup.

Fabmodules is installed in a Linux VM running in Virtual Box on the laser cutter machine.

Starting
---------

To start the Linux machine, run "fabmodules-ubuntu-1404" from the Windows desktop.

When inside the VM, run "fabmodules" from the Linux desktop.


Sharing documents
-------------------

The Windows folder "Documents" is shared to the Linux machine.
Drop files there, and go to Documents -> sf_Documents in the Linux machine to find it.

Notes
--------

Note: when the VM is running, the laser cutter is not available to Windows.
You can use Devices -> USB in Virtualbox to manually connect/disconnect the device
while the virtual machine is running. You do not need to restart fabmodules to
detect printer after pluggin in again.

Password for the VM is the same as for the physical machine.
