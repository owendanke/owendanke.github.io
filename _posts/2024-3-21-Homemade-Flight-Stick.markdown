---
layout: post
title: Homemade Flight Stick
description: I built a flight stick for games and simulators!
date: 2024-3-21
tags: [projects,hotas]
---

![Image](/assets/images/joystick_final_1.jpg)

People typically refer to this as a joystick, but flight stick sounds a lot cooler. This project took the better part of a year to build, but I still don't consider it finished (the base needs paint at the very least!).

What this joystick features is a replacable grip that houses two shift registers which can accomodate up to sixteen buttons. The base holds an "Arduino Pro Micro", sporting an ATmega32u4 and native USB support.

The X and Y axis of the joystick base use magnetic position sensing through 49E hall effect sensors. I should have just borrowed someone's design for a magnet and sensor holder because experimenting with different magnet/sensor positions and holders took some time.
My design does work and has proven stable so I am quite pleased that it worked out. 


Credit where credit is due:
 - B8 grip model came from [hc625ma]'s GitHub
 - Joystick base is [rdbeerman]'s modification of [olukelo]'s design
 - Shift register PCB is by [Debolestis] modified to fit the 74HC165 instead of the CD4021
 - Joystick Arduino library by [MHeironimus]

I started with the SLDPRT B8 style grip, but I had seen a photo of one with a toggle swith on the top right in addition to the push button on the left.
I used OnShape to model everything, I sought after projects that included files like SLDPRT because they are the actual model contrary to STL which is an approximation.
This makes it much easier to remix designs.

I also reduced the number of screw holes and changed the internal geometry to fit my needs.
I unfortunately I still made it slightly to tight so the sides don't close perfectly.
A technique I learned after this project, which I will use in future projects, is to give the matching faces an *L* shape lip so the seam is less pronounced and imperfections are hidden.

![Image](/assets/images/IMG_3143.jpg)

Inside the grip I house a shift register board.
What this accomplishes is reducing the number of wires from the base to the grip.
With one of these I only need five wires, including ground, to exist between the two pieces.
Many of other HOTAS projects use the CD4021 shift register
At the time I had 74HC165 and that is what I used, they both do the same thing, parallel in shift out.

When modifying the grip I thought it would be cool to have a double action trigger, pull half way down for one input and all the way down for the second input.
I only have the one action right now for this grip.
I will probably just make another grip for other games before I get around to adding the second trigger action.

![Image](/assets/images/IMG_3192.jpg)

My design for holding the 49E hall effect sensors could be improved, but more importantly, it works and gives suprisingly good resolution.
Resolution here is the change in resistance, or measured voltage, for the observed magnetic field.
The magnetic polarity is utilized as I found it was easier to design when the magnetic pole normal vector was pointing to (or away idk) the sensor.
This design makes the hall sensor increase resistance when the normal points one way, and decreases resistance when the normal vector points the opposite direction.
I am being vague here because I forget the specifics, and one axis is reversed compared to the other.

![Image](/assets/images/IMG_3191.jpg)

The base holds the "Arduino Pro Micro", an ATmega32u4 based board, and communicates to the shift register through the 6 pin DIN located in the shaft.
I used a joystick library by [MHeironimus] because it worked with the Arduino IDE and is very simple to use.


![Image](/assets/images/IMG_3188.jpg)


[olukelo]: https://www.thingiverse.com/thing:2496028
[hc625ma]: https://github.com/hc625ma/simchair_models/tree/master/Components/Peripherals/B8%20flight%20stick
[rdbeerman]: https://github.com/rdbeerman/Joystick-Gimbal
[Debolestis]: https://oshpark.com/shared_projects/CNmz8HuL
[MHeironimus]: https://github.com/MHeironimus/ArduinoJoystickLibrary