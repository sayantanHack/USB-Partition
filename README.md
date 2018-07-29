# USB-Partition
This repo is for USB Partitioning using linux

## How to fix this USB Partition error
There have few cases when USB got parted into multiple partiions . To fix this justplug the usb pendrive in then follow the bellow commands.

## sudo su
## fdisk -l
## umount /dev/DEVICE
## shred -vf -n 3 /dev/DEVICE
## parted /dev/DEVICE
## mktable msdos
## mkpart primary 0% 100%
## quit
## mkfs.msdos -F 32 /dev/DEVICE1

here DEVICE is your usb drive name like /deve/sdb or /dev/sdc or /dev/sdd etc
