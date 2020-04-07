Use the script from [here](https://bugzilla.kernel.org/show_bug.cgi?id=61651).

automatic dkms module installer for patched alx

This is a quick and dirty setup that will automatically setup the dkms module for your specific kernel version.
This will only work on debian/ubuntu and other derivates and requires dkms and patch to be setup already.

The setup uses sudo and thus you are asked for your password once.
It will then attempt to download your kernels source, copy and patch the alx related files and place a "alx-<kernel-version>" in your /usr/src directory, enable and compile the module and finally rebuild your initrd.  
Currently the the very first compilation somehow fails, thats why it's run twice.