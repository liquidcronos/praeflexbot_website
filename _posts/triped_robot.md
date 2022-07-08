---
permalink: /docs/robot/
title: "TriPed Robot"
layout: single
excerpt: "Each Leg of the TriPed hase 3 degrees of freedom allowing ..."
collection: docs
layouts_gallery:
  - url: triped_web_banner.png
    image_path: triped_web_banner.png
    alt: "triped web banner"
toc: true
---

The TriPed is a new three legged Robot, in development at Heidelberg university.
The System consists of three independent, one-legged sub-robots pictured below, which are connected by a common platform. 
The aim of the TriPed project is to develop working and robust decentralized walking systems.
![Triped game](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/triped_game.png)

The term decentralized walking system,  refers to a system in which multiple one legged robots must cooperate in order to successfully produce a stable gait.
Since such a controller makes no assumptions about the whole system dynamics, it should be reusable in multiple systems without retuning.

While this is useful for the modular design of walking robots, the primary application can be expected to be in the medical field.
There, the legs could be used in order to automate crutches.

## Functional parts
A complete Overview over the functional parts and their naming conventions can be seen in the figure below.
More detail about the hardware is provided in [Chassis](https://triped-robot.github.io/docs/chassis/) and [Legs](https://triped-robot.github.io/docs/legs/).
The Required Embedded hardware to interface with the system is explained in [Embedded Architecture](https://triped-robot.github.io/docs/embedded/), while the page [Kinematic Model](https://triped-robot.github.io/docs/kinematics/) describes 
how the TriPeds motors have to move in order to move the feet in a given way.
Lastly the section [Safety Guidelines](https://triped-robot.github.io/docs/safety/) provides Guidelines for working with the hardware in a safe manner.

![functional components](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/naming_conventions.png)

## History of the TriPed
The TriPed was first envisioned by Professor Badreddin in 2002 as a nonbiomimetic robot.
Meaning a robot, unlike conventional walking machines, is not inspired by animals but instead the fundamental principles of walking.

It has 3 legs because that's all you need to stand stably. It doesn't have knees because those are only needed for crouching and climbing not walking itself.
The first theoretical research on the TriPed considered how such a system could feasibly walk.
The Original Version however was never build.

When in 2019 a new research cooperation between Professor Badreddins <a href="https://www.ziti.uni-heidelberg.de/ziti/en/institute/research/38-ziti-group/menue/560-automation-laboratory">automation lab</a>, Professor Masias  <a href="https://www.lorenzomasia.com/lab-and-people">aries lab</a> and Professor Peter Potts 
<a href="https://www.imt.uni-stuttgart.de/en/">Institute of Medical Device Technology </a> had need for a demonstrator, a new version of the robot was disgned and build by Peter Potts team and delivered to Heidelberg.
Since Professor Badreddin is now an emeritus, the new TriPed robot is now officially part of the Aries lab.

![old triped](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/triped_asm.jpg)
