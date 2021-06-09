---
permalink: /docs/kinematics/
title: "Kinematic Model"
layout: single
collection: docs
layouts_gallery:
  - url: triped_web_banner.png
    image_path: triped_web_banner.png
    alt: "triped web banner"
toc: true
---

This section offers a short overview of the kinematics as well as important coordinate systems of the TriPed.\\
It assumes that one is already familiar with robotic kinematics and the general terminology. If this is not the case, [this page](http://motion.cs.illinois.edu/RoboticSystems/Kinematics.html) offers a short tutorial.

## Kinematic Structure of a Leg
Each leg is a so called hybrid chain whose kinematic structure is pictured below.

The different colors of the figure aim to highlight the multiple different transformations that lead to the same coordinate system.\\
Since the three colored parts at the top all lead to the leg linear part of the leg, they form a closed chain, while the leg linear part itself is an open chain.\\

![triped_joints](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/triped_leg_joints.png)

The hybrid nature (specifically the closed subchain) of the system has many repercussions in terms of th kinematic calculations as well as available control strategies.

These are discussed in the last section.

## Coordinate Frames

This sections provdes conventions and standarts for the robots coordinate frames.
Note that the TriPed does not use the popular [Denavit Hartenberg Conventions](https://de.wikipedia.org/wiki/Denavit-Hartenberg-Transformation) as these arenot suited for closed kinematic chains.
The Coordinate Frames of the TriPed instead adhere to the following conventions:

- Each frame is represented by a right-handed coordinate system
- the orientation of this coordinate system is specified using [quaternions](https://de.wikipedia.org/wiki/Quaternion)
- https://de.wikipedia.org/wiki/Quaternion
- The transformations between connected Frames is defines through a homogeneous transformation A<sup>old</sup><sub>new</sub>

Meanwhile the transformations of joints adopt the following conventions:

- Each joint is specified by a base and a follower frame
- The base frame is located at the position of the joint.
- The transformation between base and follower frame is performed by the joint
- Joints with single degrees of freedom actuate around the Z axis.

The resulting frames and their naming conventions can be seen down below.
A blue frame represents a base frame and a orange frame a follower frame.
![triped_joints](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/coord_systems_bottom.png)


## Closure Equation



