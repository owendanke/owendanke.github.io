---
layout: post
title: "Homemade Flight Stick"
description: "I built a flight stick for games and simulators!"
date: 2025-07-08
feature_image: images/joystick_final_1.jpg
tags: [projects,hotas]
---

People typically refer to this as a joystick, but flight stick sounds a lot cooler. This project took the better part of a year to build, but I still don't consider it finished (the base needs paint at the very least!).
What this joystick features is a replacable grip that houses two shift registers which can accomodate up to sixteen buttons. The base holds an Amazon special "Arduino Pro Micro", sporting an ATmega32u4 and native USB support.
The X and Y axis of the joystick base use magnetic position sensing through 49E hall effect sensors. I should have just borrowed someone's design for a magnet and sensor holder because experimenting with different magnet/sensor positions and holders took some time.
My design does work and has proven stable so I am quite pleased that it worked out. I'll go into detail about the build, design decisions, and software (briefly) below.
