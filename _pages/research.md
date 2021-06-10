---
permalink: /research/
title: "Research"
layout: single
excerpt: "The TriPed is a 3 legged Robot investigating human-machine /machine-machine cooperation"
layouts_gallery:
  - url: triped_web_banner.png
    image_path: triped_web_banner.png
    alt: "triped web banner"
toc: true
---

Traditional assistive devices model the human as some kind of operator whose commands should be followed.
However, these approaches don't work for more assistive devices where both device and operator have to rely on one another.
Thus the human can no longer be thought of as an operator but as an equal player cooperating with the machine.

But Humans tend to cooperate differently than machines do.
While machines cooperate by exchanging plans and information at incredible speeds, humans tend to infer and coordinate using subtle cues from their partners often without needing to directly exchange information.

The goal of this project is to close this gap by enabling machines to cooperate as humans do.

This in turn would aid human-machine cooperation, because the human can then naturally interact with the machine.


## Modelling Cooperation
In the case of the TriPed each Leg can be viewed as a separate subsystem with only limited information about the other systems.
![triped robot](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/triped_game.png)

The questions the TriPed should help answer are:
- How can multiple systems cooperate without directly communicating?
- What type of information can be inferred from the behavior of the other systems?
- What kind of sensor information is needed for both?

The cooperation is modeled  using a simplified interaction model which abstracts each player to a set of forces and constraints he can impart on the system <br>
Using Gametheoretic Approaches borrowed from game theory, particularly <a href="https://en.wikipedia.org/wiki/Behavioral_game_theory"> behavioral game theory</a>.
These approaches cannot only model the interplay of each agent but also a process called "signaling" in which agents communicate their intention to one another through their strategic play. 

## Supernumerary Limbs
These findings should eventually be used to help build new kinds of assistive devices.
Traditional assistive devices model the human as some kind of operator whose commands should be followed.

This approach doesn't work for automatic crutches, consider for example the cases of walking and stumbling. The machine should allow and facilitate the first kind of movement but prohibit the second type.
Thus the human can no longer be thought of as an operator but as an equal player cooperating with the machine.\\

It is known that the rehabilitation phase after an operation is as important as the
operation itself.
In the case of major abdominal operations or longer periods of bed rest, the patient often has to learn to walk again.
Since the use of crutches inhibits the use of a patient’s hands, if they can use
them at all, supernumerary limbs exosuits should provide automatic crutches that walk without human command.\\
\\
The TriPed Plattform can emulate such a configuration by considering two of its legs as crutches controlled by its controller, while the third leg imitates a single human leg.
The assumption here is, that the human isn't able to use his third leg because of some injury.

A sample rendering of such a system can be seen down below
![triped robot](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/research_aim.png)



## Control of Hybrid Chains
Even with a central agent controlling everything, the control of walking robots is a hard task. 
For this reason, we are also interested in the general control of walking robots.
Our particular area of focus is the control of so-called hybrid kinematic chains which are mechanism with both closed kinematic chains and open kinematic chains.
In the case of the TriPed each sub-robot is a hybrid chain.
![level mechanism](https://raw.githubusercontent.com/TriPed-Robot/TriPed-Robot.github.io/master/images/hybrid_chain.png)

---

