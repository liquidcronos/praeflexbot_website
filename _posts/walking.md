---
permalink: /docs/walking/
title: "Walking on three legs"
layout: single

collection: docs
layouts_gallery:
  - url: triped_web_banner.png
    image_path: triped_web_banner.png
    alt: "triped web banner"
toc: true
---

Since the TriPed is one of the view three-legged robots around, the question arises:

How can a three-legged robot even walk?


While there are no three-legged animals in nature, many animals use a Tripedal gait.
Thus a few gaits can be devised inspired by nature.



## Rabbit Hopping Gait

Although a rabbit posses four legs during hopping its two front legs act like a single leg.
This gait is quite fast and alows the robot to move forward and turn at the same time.
This means it is able to follow a given linear velocity and angular velocity.
The stance pattern of this gait can be seen below:
![rabbit gait](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/rabbit_gait.gif)


## Spider Walking Gait
This is the most stable gait of the TriPed since only one foot moves at a time.
It is inspired by the cyclical way in which spiders move the leg on each side of their body.
In the case of the TriPed all legs walk in a clockwise fashion.
While slower than the rabbit gait, it allows the system to move in any direction without turning.
It can be seen down below:
![spider walking gait](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/triped_walking.gif)

There is also an interactive demo which can be found [here](https://triped-robot.github.io/docs/matlab_getting_started/)

## Other Gaits
There are a large number of additional walking gaits including but not limited to:
- Dog-style cruising gait
- Kangaroo-style hopping gait


On top of which there are severall running gaits.
However, all these have only been investigated theoretically and so far not been tested on the TriPed.
Indeed it is likely that the kangaroo-style gait would not work due to the tripeds limited task space.


The gait pattern graph for each gaut can be seen down below:
![gait patterns](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/gait_patterns.png)




## Weight Redistribution
Apart from the multitude of possible gait patterns, it is also important to consider what each leg does while it is on the ground.
To be able to even lift a leg, the system needs a mechanism to redistribute weight to the other leg.\\
This can be done in one of two ways:
- changing the orientation of the chassis
- changing the position of the chassis relative to the legs.

Most legged robots use the first approach since the design of their legs makes a free horizontal movement of the body difficult.
Due to the round design of the TriPed however, it can also employ the second strategy.
This is done for example in the spider gait, where the chassis moves in a circle.