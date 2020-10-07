---
permalink: /research/
title: "About"
layout: single
excerpt: "The TriPed is a 3 legged Robot investigating human machine /machine machine cooperation"
layouts_gallery:
  - url: triped_web_banner.png
    image_path: triped_web_banner.png
    alt: "triped web banner"
toc: true
---

# History
The TriPed was first invisioned by Professor Badreddin in 2002 as a non biomimetic robot.
Meaning a robot, which unlike conventional walking machines, is not inspired by animals but instead the fundamental principles of walking.

It has 3 legs, because thats all you need to stabily stand. It doesnt have knees because those are only needed for crouching and climbing not walking itself.
The first theoretical research on the TriPed considered how such a system could feasibly walk.
The Original Version however was never build.

When in 2019 a new research cooperation between Professor Badreddins <a href="https://www.ziti.uni-heidelberg.de/ziti/en/institute/research/38-ziti-group/menue/560-automation-laboratory">automation lab</a>, Professor Masias  <a href="https://www.lorenzomasia.com/lab-and-people">aries lab</a> and Professor Peter Potts 
<a href="https://www.imt.uni-stuttgart.de/en/">Institute of Medical Device Technology </a> had need for a demonstrator, a new version of the robot was build by Peter Potts team and delivered to Heidelberg.
Since Professor Badreddin has retired, the TriPed robot now serves as part of the Aries lab.

![old triped](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/triped_asm.jpg)

# Research
## Ultimate Research Aim
<p>It is known that the rehabilitation phase after an operation is as important as the operation itself.<br>
In the case of major abdominal operations or longer periods of bed rest, the patient often has to learn to walk again.
As a consequence, patients are still dependent on crutches for weeks after the operation.<br>
 However, some patients might not be able to use them due to cognitive or arm impairments, and even if, these severely restrict their everyday life, 
 as the crutches prevent them from using their hands for other purposes.</p>

<p> The ultimate aim of this project is to develop autonomous crutches that lift those restrictions and help the patients regain a normal life.
The device should also be able to be used as a rehabilitation device that trains the patient on how to walk again. </p>
![research aim](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/research_aim.png)

## But why a Robot?
<p>
Traditional assistive devices model the human as some kind of operator whose commands should be followed <br>
This approach doesn't work for automatic crutches, consider for example the cases of walking and stumbling. The machine should allow and facilitate the first kind of movement but prohibit the second type.
Thus the human can no longer be thought of as an operator but as an equal player cooperating with the machine. </p> 

<p> Which is why we need to understand cooperation between different agents first before we can develop autonomous crutches. <br>
This is where the Triped comes in. The Robotic platform allows us to study the principles of cooperative walking by dividing the System into three autonomous "Players".
Among our interests are not only what kind of sensory information each player needs to cooperate with the other ones but most importantly how they can coordinate themself to cooperate efficiently without directly exchaning data. 
</p>
![triped robot](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/triped_game.png)

## Modelling Cooperation
We Aim to model the cooperation of Human and Machine using a simplified interaction model which abstracts each player to a set of forces and constraints he can impart on the system <br>
Using Gametheoretic Approaches borrowed from game theory, particularly <a href="https://en.wikipedia.org/wiki/Behavioral_game_theory"> behavioral game theory</a> we intend to model not only the interplay of each agent but also a process called "signaling" in which agents communicate their intention to one another through their strategic play. 


## Walking Robot Control
Even with a central agent controlling everything, the control of walking robots is a hard task. 
For this reason, we are also interested in the general control of walking robots.
Our particular area of focus is the control of so-called closed kinematic chains which are configurations where multiple actuators influence the same endpoint.
This is not only because the Triped itself can be thought of as a closed kinematic but also because each subrobot uses a closed kinematic chain to swing its leg.
![level mechanism](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/Hebel_1.PNG)

---

