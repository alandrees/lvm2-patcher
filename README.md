lvm2-patcher
============

Bugreport: https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=741652

This is a small bash script &amp; patch for the lvm2 bug in debian testing. 

If you are currently running your root filesystem from an lvm volume, upgrading to debian jessie right at the moment will
break the boot process.

Anytime this happens, you'll be prompted because it won't be able to find your lvm root partition.

When given the initramfs prompt, you can enter

>lvm vgchange -ay

This will get you back into your system.

This script applies the patch and updates your initramfs with the updated file.
