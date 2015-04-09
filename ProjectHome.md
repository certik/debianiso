Easily customisable robust Debian boot CD scripts.

  * Uses pbuilder (a standard tool) for creating the base system
  * allows you to edit the base system (install more packages using apt-get, edit files...)
  * creates an iso image (you can test it in qemu)
  * after booting, it drops you into the busybox, with instructions how to proceed - you need to mount the cdrom (usb stick, whatever) manually (so that you can always boot it)
  * boots the rest of the system automatically

# Why another Debian boot CD? #

There are other similar projects (see the links), however this project's motivation is:

  * simplicity: just a simple short bash script, doing things you would do by hand, if you wanted to create the boot CD (thus you can do it automatically but also you can modify it to suit your needs perfectly)
  * robustness: you do all the vulnerable steps that can fail by hand (creating the base system, adding extra packages, locating the base.tar.bz2 after booting), so that you can always easily fix it and you can boot from all kinds of CDs and USB sticks, as long as you are able to mount the drive in the shell from the kernel, that you installed on the image

See for yourself, browse the code from svn [here](http://debianiso.googlecode.com/svn/trunk/).

# Installation and usage #

See the README file in the repository:
```
svn co http://debianiso.googlecode.com/svn/trunk/ debianiso
cd debianiso
vim README
```

## Tips ##

Install manually those packages, that you need (xfs utils, debootstrap, ...), boot from the CD, connect to the internet, install anything you might need on the live system, use debootstrap to install debian (see DebootstrapInstructions) on the disk.