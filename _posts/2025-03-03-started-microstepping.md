---
layout: post
title:  "Starting with Microstepping"
braille-title: "⠠⠌⠜⠞⠬⠀⠾⠀⠠⠍⠊⠉⠗⠕⠌⠑⠏⠏⠬"
date:   2025-02-21 9:45:00 -0500
---

Worrying about physical things can be strange for a gaggle of computer scientists. 
Our training and disposition is to be obsessed with the virtual--that which we can 
build up from raw bits to our own liking and rules. But when stepper motors make loud 
clicking, clanking sounds and don't properly move, it takes no genius to know that poor 
engineering is present.

Stepper motors work by energizing certain "stator poles"" and thus rotating the "rotor poles", 
and connected shaft, by force of magnetic attraction and repulsion. Here is an image 
of the insides of a stepper motor for reference.

![Stepper Motor Diagram]({{ "/assets/images/stepper-motor-diagram.jpg" | relative_url }})

Each opposite pair of stator poles is run by a separate DC power supply that, when 
all working in tandem, produce an accurate control of the shaft.

This sounds all well and good, especially for CS students, but the rotor poles magnetically snap 
into place when run and try to hold their position. Trying to run them quickly with the mechanical 
load of the print head led to the stepper motors sounding as though they were breaking and 
occasionally slipping, missing a step.

However, as each each stator pole is itself an inductive load, they can be PWMed for even finer 
control. This approach is known as "microstepping", or stepping a fraction of a full step at a time. 
Not only does the allow for finer control of shaft's position, but also runs the motors much smoother 
than trying to execute many full steps per second.

There is perhaps a more generally valuable lesson in this problem for the virtual-oriented: 
to remember that our virtual systems always have physical consequences. While more obvious when 
writing code to drive *loud* mechanical components like motors and solenoids, we 
would do well to remember our code always drives some silent processing unit. Every instruction run, 
virtual world hosted, or model trained is but the sleepless dream of a CPU, which at the least is consuming electricity and producing heat.

As much as we may feel our virtual creations are separate or running in tandem to the tangible world, they 
simply are not. Perhaps we should more concerned with the physical; it may be that is all that 
ultimately matters. Less poetically, it seems at least our due diligence to remember such consequences exist.

