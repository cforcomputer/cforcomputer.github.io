---
layout: post
title: internet radio
slug: internet-radio
---

skills used:
- Arduino (C++)
- Prompt Engineering
- 3D CAD (Onshape)
- 3D Printing
- Electrical

[view project code](https://github.com/cforcomputer/TTGOInternetRadio)

### Internet radio project

#### My introduction to hardware prototyping

[![Internet radio demo](assets/images/projects/radio-prototypes.jpg)]()
*Click the image to watch a demo video.* (has not been created yet)

The internet radio was one of my first serious CAD projects where I attempted to build a fun enclosure for a full featured internet radio.
It uses a TTGO V1 display which is a modified ESP32. It looked like a fun board to mess with, but if I were to do the project over I'd have 
gone with the newest ESP32 chip. (just for the sake of being able to use all the up-to-date libraries).

The radio can:
1. Act as a bluetooth speaker or BT to 3.5mm adapter
2. Create a wifi configuration portal
3. Allow the user to add any internet radio station
4. Act as a visualizer for music

I was surprised by how few working internet radio project there were. Most of the examples that I found were no longer functional or too limited. 
I forked a project that I found on youtube, but it was non-functional and I ended up redoing the entire thing with a different audio library.

![CAD drawing in Onshape](assets/images/projects/radio3d.png)
I used Onshape for the 3D component of this project, and went through many iterations of the enclosure before I landed on one that was fully usable. 
I was surprised by how long it takes to find the perfect positioning for all the buttons. I have a newfound respect for simple builds, it takes a lot
of time investment to get it right.

The bluetooth pairing to my phone and pc works flawlessly. 
![Internet radio bluetooth mode](assets/images/projects/radio-bluetooth.jpg)

WIP post. more TBA