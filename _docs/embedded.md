---
permalink: /docs/embedded/
title: "Embedded Architecture"
layout: single
collection: docs
layouts_gallery:
  - url: triped_web_banner.png
    image_path: triped_web_banner.png
    alt: "triped web banner"
toc: true
---



Since the TriPed is a tool to study the collaboration of different systems, it was decided, that each sub-robot should have its own independent control PC.
However some tasks such as initialization, safety monitoringor information sharing on the gait generator level requires high-level communication between the sub-robots.\\
For this reason, each controller needs a way to communicate with the other ones as well as with a remote monitor from which the operator can supervise the system.\\
\\
Because the remote monitor is not part of the robot itself but an independent desktop PC in the same lab, the communication should be wireless.\\
In the end, it was decided to implement this communication over WLAN, with a dedicated network router in the lab responsible for the communication.\\
A schematic of this high level architecture can be seen below

![high level communication](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/full_control_network.png)

# Leg Level Architecture
Each Leg needs to be able to connect four devices via CAN Bus and SPI respectively.
Additionally the Extend Sensor requires many system interrupts per second putting stress on the control pc.
The System uses a Beaglebone Black to connect all these Devices, however although it has a dedicated chip for dealing with rotary encoders,
the Extend Sensor is abstracted using a additional Arduino. This is done to be easily able to transition to a more powerful control pc should the need arise.
A general high level wiring scheme can be seen down below
![abstract wiring scheme](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/Verdrahtungsschema.png)

This abstract wiring scheme is implemented using a custom cape seen below which is stacked upon a [can cape](https://www.waveshare.com/wiki/RS485_CAN_CAPE)

![beaglebone cape](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/bbb_cape.png)

