---
permalink: /docs/getting_started/
title: "Getting Started"
layout: single

collection: docs
layouts_gallery:
  - url: triped_web_banner.png
    image_path: triped_web_banner.png
    alt: "triped web banner"
toc: true
---

This Page describes how one can interact with the TriPed from a software standpoint.
It starts with a guide on how to set up the Beaglebone followed by instructions on how to interact with the system and start its various components
# Beaglebone Setup

## Installing the Operating System
The Beaglebone uses the debian buster iot edition, which installed on the eMMC.
To install it download the flashing image [here](https://debian.beagleboard.org/images/bone-eMMC-flasher-debian-10.3-iot-armhf-2020-04-06-4gb.img.xz]).

The image has then be installed on a sd and subsequently installed on the BBB.
A good tutorial can be found [here](http://derekmolloy.ie/write-a-new-image-to-the-beaglebone-black/).


## Patching the Kernel with Xenomai

## Mounting the SD card
After installing the operating system, the SD card can be flashed with the internal TriPed image that has all necessairy ros-packages pre installed.

To access these files, the SD card has to be mounted. This is done by opening `/etc/fstab` using
```
sudo nano /etc/fstab
```

And appending the line
```
/dev/mmcblk0p1 /sd auto rw,user,auto,exec,nofail 0 0
```

Afterwards the ownership of the SD card neesd to be altered to allow seemless writing and reading
```
sudo chown -R debian:debian /sd
```

## Creating a Swap Partition
The `catkin_make` process which compiles the ROS code can be resource intensive.
For this purpose it is advisable to create a swap partition.
There are severall tutorials on how to do this, such as [here](https://paulbupejr.com/adding-swap-memory-to-the-beaglebone-black/).
A swap file of 1Gb size is more than sufficient.

## Disabling HDMI
To use all SPI ports of the Beaglebone the HDMI port has to be disabled.
This is done by editing the file `/boot/uEnv.txt` and uncommenting the line `disable_uboot_overlay_video=1`


## Sourcing ROS enviroment
In order to immediately acces the ROS commands upon connecting via ssh and communicate ROS topics via multiple systems, the following lines have to be appended to the `.bashrc` file:
```
source /sd/triped_app/catkin_ws/devel/setup.bash
export ROS_IP=BEAGLEBONE_IP
export ROS_MASTER_URI=http://BEAGLEBONE_NAME:11311
```
where `BEAGLEBONE_IP` and `BEAGLEBONE_NAME` are the Beaglebones network IP and name respectively.


