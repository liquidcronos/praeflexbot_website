---
permalink: /docs/matlab_getting_started/
title: "Getting Started"
layout: single

collection: docs
layouts_gallery:
  - url: triped_web_banner.png
    image_path: triped_web_banner.png
    alt: "triped web banner"
toc: true
---


## Getting Matlab

The simulation runs in Matlab version 2021a.
Unfortunately, Matlab is neither open source nor free, however, if you are a student a lot of universities will supply you with a license for free.


Checkout Matlabs [website](https://de.mathworks.com/products/get-matlab.html) to find out if you are eligible

Furthermore, the following Toolboxes are required:

- simscape multibody
- phased array system toolbox
- optimization toolbox
- ros toolbox

## Getting the Code

The simulation can be installed from Github by calling
```
git clone https://github.com/TriPed-Robot/Matlab-Simulation.git
```

In a terminal, or clicking on the green button labeled `Code` to download a zip archive.


## Using the Library

You can either directly use the library by starting the Simulink package `TripedLibrary.slx` and dragging the needed files from the Simulink model into your projects.

However, the better solution would be to properly install the library by following the following [tutorial](https://de.mathworks.com/help/simulink/ug/adding-libraries-to-the-library-browser.html).




## Trying the Examples

The examples directory contains several examples to familiarise oneself with the robot and play around with it.


### Moving the Chassis
![walking example](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/walking_example.png)
This example demonstrates whole-body kinematics, meaning the ability to control the orientation of the body given positions of the leg.
To use the example open `joy_stick_orientation.slx` and connect a gamepad (such as an XBox controller).
If you play the Simulink model you will be able to move the TriPeds chassis with your joystick causing the robot to 'look around'.
Alternatively, if you don't have a joystick you can connect any signal to the roll pitch and yaw inputs of the full-body kinematics block.


### Moving the TriPed
![orientation example](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/orientation_example.png)
This example demonstrates how the TriPed can walk. Using the left joystick of a connected gamepad it is possible to steer the TriPed around the simulation area.
Alternatively, if you don't have a joystick you can directly specify a two-dimensional command velocity to the gait generator.
The example can be started by opening and playing  `joy_stick_walking.slx`.

### Following Positions
The TriPed is not only able to follow a given command velocity but also to move to a desired position.
For the real robot, this requires position estimating techniques such as [SLAM](https://de.wikipedia.org/wiki/Simultaneous_Localization_and_Mapping), in this case, the simulation itself provides the position feedback.

In the example `position_control.slx` the TriPed uses a position controller to follow a blue ball around a map.
This example needs no external input and will run on its own. new trajectories can be provided by changing the `Circular trajectory` function block. 

