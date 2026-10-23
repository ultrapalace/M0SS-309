v1.1 - Aug 18th, 2026.  
  
- bug fix: voice stealing pops - modify voice stealing algo to add kill phase.  
- reduce dsp chunk size to 512.  
- set FX .dsp sample rate to match main .dsp.
  
### NOTE
This firmware also requires to update config.txt on the SD Card, or you will get some glitching after 60 seconds.

on line 15 add `force_turbo=1`

The file should now read:
```
#
# Enable 32-bit mode (AArch32)
#
# This file must be copied along with the generated kernel7[l].img
# onto a SD(HC) card with FAT file system, if 32-bit mode is used.
#
# This file also enables the possibility to use the FIQ and two
# displays with the Raspberry Pi 4 and selects the required mode
# for the USB host controller of the Compute Module 4.
#

arm_64bit=0
kernel=kernel8-32.img
device_tree=bcm2710-rpi-cm0.dtb
force_turbo=1

[pi4]
kernel=kernel7l.img
armstub=armstub7-rpi4.bin
max_framebuffers=2

[cm4]
otg_mode=1
```