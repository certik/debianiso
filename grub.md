
```
apt-get install grub
mkdir /boot/grub
cp /usr/lib/grub/i386-pc/* /boot/grub/
```
the file `stage2_eltorito` is not really needed in `/boot/grub`, but who cares...
```
update-grub
grub
root (hd0,2)
setup (hd0)
quit
```
where "`hd0,2`" is the filesystem containing the `/boot/grub` directory. Everything is harmless, except the "`setup (hd0)`" command, which installs grub into the MBR. If it doesn't work from chroot, try it from Knoppix, or boot into grub and do it again.