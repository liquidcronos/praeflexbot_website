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

## Xenomai
Xenomai is a real-time development framework cooperating with the
Linux kernel. It is seamlessly integrated into the standard Linux en-
vironment and provides a separate high priority interrupt pipeline. 

Xenomai allows to directly specify the time a task should take.

While Xenomai allows the real-time implementation of multiple pro-
cesses, the communication structure between these processes has to be
explicitly designed. 

Implementing a custom communication scheme is a
complicated task requiring in depth knowledge of parallel systems. 

To simplify this process and fulfill the second requirement one can employ
a standardized message passing interface which abstracts and simplifies
the communications.

There are many popular message-passing solutions, however, for robotic
applications the most common solution is ROS which is quickly be-
coming an industry standard.
