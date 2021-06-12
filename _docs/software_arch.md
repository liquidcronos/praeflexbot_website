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
For this the robot operating system ROS was choosen.
ROS abstracts the communication between independent processes, called nodes, by employing its own
message passing interface.
More information about ROS can be found [here](http://wiki.ros.org/).


## High Level Architecture
Since each Leg is independent from the rest, they each have their own architecture.
However for safety reasons all three software stacks are monitored using a event manager.
This manager has the activate and deactivate nodes according to the needs and safety of the overall system.


The architecture of each leg decomposes the full control loop of the system into multiple independend nodes under considerations of possible parallelism and communication overhead.
In short, the system should make use of as much parallelism as possible while keeping the communication overhead as small as possible.

Since a huge network of independent nodes obfuscates the true
control structure these nodes are grouped into packages according to the loop
from which they hail. This leads to a layered architecture of Node
Groups:

![layerd arch](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/layers.png)

The following sections will provide a short overview over the purpose of each layer. 
However the full documentation for each layer is provided in their packages code documentation.


## Joint Level Control 

The joint level control layer implements the decentralized joint space
control of each joint. It handles the load compensations and accepts de-
sired joint values as well as feed-forward values as inputs.

The package can be found here [here](https://github.com/TriPed-Robot/joint_level_control)

## Leg Level Control

The leg level control Layer implements the leg control in task space.
This means the System is responsible for computing the forward and inverse kinematics as well as the feedforward velocity and torque for the joint controllers.

Additionally, the leg level control layer deals with the initialization of
the robot in conjunction with the event manager.

The package can be found here [here](https://github.com/TriPed-Robot/leg_level_control) (currently only visible for project members)

## Kinematic Gait Generator

The Kinematic Gait Generator is the highest level Controller of each sub-robot.
It is responsible for deciding when and how each leg makes a step, and what it does in between steps.

The package can be found here [here](https://github.com/TriPed-Robot/kinematik_gait_generator) (currently only visible for project members)

## Signaling Game

The signaling Game layer implements the game theory based controller responsible for coordinating the legs and infer the intention of the other sub-robots.

The package can be found here [here](https://github.com/TriPed-Robot/signaling_game)  (currently only visible for project members)


