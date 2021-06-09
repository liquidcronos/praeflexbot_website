---
permalink: /docs/software_arch/
title: "Software Architecture"
layout: single
collection: docs
layouts_gallery:
  - url: triped_web_banner.png
    image_path: triped_web_banner.png
    alt: "triped web banner"
toc: true
---

The Architecture of the TriPed Robot is focused on research and educa-
tion. This means that it must be robust to produce reliable results and
keep the robot from damaging itself or the environment, but also easily
accessible with common tools taught at the university.

The first requirement necessitates a hard real-time operating system.
which can ensure that each controller performs with a given frequency
uninterrupted by system updates and other ’distractions’ present in a
normal operating system. For this robot, Xenomai was chosen as the
Operating System of the BeagleBone Black.
More information about Xenomai can be found here.

The second requirement neccesiatates a standardized message passing interface which abstracts and simplifies the inter process communications.

There are many popular message-passing solutions, however, for robotic
applications the most common solution is ROS which is quickly be-
coming an industry standard.

## ROS

ROS abstracts the communication between independent processes, called nodes, by employing its own
message passing interface.
Like many other message-passing interfaces it can communicate not only
between processes on the same machine but also between computers.
This means that students and researchers can use wifi to remotely view
sensor data and log it for later debugging.
More information about ROS can be found [here](http://wiki.ros.org/).
