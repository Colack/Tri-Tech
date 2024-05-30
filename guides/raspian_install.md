# Installing Debian 12 Bookworm (32-Bit) to a Raspberry Pi 4

This guide is for installing Debian 12 onto a Raspberry Pi 4.

## Download the image file

Go to our class webserver, 10.183.1.26, then go to the folder labelled `iso`, then `minecraftpi`. You will want to download the file titled `2024-03-15-raspios-bookworm-armhf.img.xz`. You can also download the file from [here](raspberrypi.com/software/operating-systems/).

## Installing and Flashing to the MicroSD Card

As a non root user, extract the compressed image, `2024-03-15-raspios-bookworm-armhf.img.xz`, with the xz command: 

```
$ xz -dv 2024-03-15-raspios-bookworm-armhf.img.xz
```

Then, run the lsblk command to see what drives are connected to your Linux System. Here is a example output:

```
jackjack@joker:~$ lsblk
NAME  MAJ:MIN  RM  SIZE  RO  TYPE  MOUTPOINTS
sda    8:0     0 931.5G  0   disk
|-sda1 8:1     0 930.6G  0   part  /
|-sda2 8:2     0     1K  0   part
|-sda5 8:5     0   976M  0   part [SWAP]
sdb    8:16    0 465.8G  0   disk
|-sdb1 8:17    0 465.
