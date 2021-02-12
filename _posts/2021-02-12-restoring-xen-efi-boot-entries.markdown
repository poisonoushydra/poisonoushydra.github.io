---
layout: post
title:  "Restoring Xen EFI Boot Entries"
date:   2021-02-12
categories: jekyll update
---

# Restoring Xen EFI Boot Entries

I have experienced several recent occurences of my EFI "forgetting" the boot entries for my Xen Hypervisor (based on Alpine Linux).

Alpine is a fantastic distribution but their documentation is somewhat lacking and often outdated. This means I am continually placed in the position of having to dig up the steps I have taken in order to restore the boot entries which is generally a more tedious process than actually restoring them. To that end I have decided to document the procedure here so that I (and others) can benefit from these instructions in the future. 

Without further ado...

# The Process

I begin by using balenaEtcher to write the latest Alpine Xen .iso image to a USB stick. Please note that attempting to restore the GRUB bootloader using the Standard or Extended .iso downloads seems to fail (possibly due to a mismatched kernel version).

Once the system has booted from the flash drive the following commands are issued:

~~~~
fdisk -l
~~~~

This will show a list of disks / partitions present on the system in an effort to identify which one contains the Xen Hypervisor installation (in my case it happens to be */dev/sdd*).

Next we issue:
~~~~
mount /dev/sdd3 /mnt
mount /dev/sdd1 /mnt/boot
~~~~
to mount the root and ESP partitions respectively.

We also need to bind mount several key directories into our mounted system otherwise the later commands will fail: 

~~~~
mount -o bind /proc /mnt/proc
mount -o bind /dev /mnt/dev
mount -o bind /dev/pts /mnt/dev/pts
mount -o bind /sys /mnt/sys
~~~~


With everything mounted we are free to chroot into */mnt* with the following command:

~~~~
chroot /mnt /bin/ash 
~~~~

noting that the */bin/ash* variable can be omitted or changed depending on your shell of choice.

Now that we are inside the mounted chroot environment we can begin restoring the missing EFI entries, beginning with:

~~~~
grub-install --target=x86_64-efi --efi-directory=/mnt/boot --bootloader-id=alpine
~~~~

Feel free to replace the *--bootloader-id=* variable with whatever name you would like to appear in your system's boot menu.

The command should notify you that it was completed without errors.

Next we issue:

~~~~
grub-mkconfig -o /boot/grub/grub.cfg
~~~~

to make sure any options we have configured in */etc/default/grub* are passed to the bootloader upon rebooting. The *grub-mkconfig* command should also notify us that it was completed without errors.

We can use the command:

~~~~
efibootmgr
~~~~

to verify that the EFI boot entry was written successfully.

Next we issue the standard command:

~~~~
reboot
~~~~

with our fingers crossed, selecting the newly created *alpine* entry from our motherboard's boot menu. 

If everything went smoothly our Xen Hypervisor GRUB menu should appear shortly and subsequently boot our Xen dom0 instance!

