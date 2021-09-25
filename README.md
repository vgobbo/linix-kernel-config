# Linux Kernel Configs

Linux kernel configurations I use in my computers.

## Gentoo

One-iner to build with LVM encrypted support:
```bash
nice -n 19 make -j 24 && make modules_install && make install && nice -n 19 genkernel --lvm --luks --kernel-config=/usr/src/linux/.config initramfs && emerge @module-rebuild && grub-mkconfig -o /boot/grub/grub.cfg
```
