---
layout: post
title:  "Fujitsu Keyboard"
date:   2020-01-18 09:45:20 -0500
categories: project
permalink: /projects/Fujitsu_Keyboard/
---


![Fujitsu1](/img/fujitsukeyboard1.JPG)

A few months ago I was Looking though a thrift shop and I found this 90s keyboard with nice feeling switches. I bought it and planed on using it for my desktop computer. However this keyboard uses the AT 5-pin DIN connector, so it is not as simple as buying a passive adapter and plugging everything together and calling it a day. This is how I made it work.

<img src="/img/fujitsukeyboard3.JPG" alt="Fujitsu3" width="400"/>

## Parts List
  * [Fujitsu FKB4700](http://telcontar.net/KBK/Fujitsu/FKB4700)
  * [Teensy 2.0 USB Development Board](https://www.pjrc.com/store/teensy.html)
  * Panel Mount USB B Socket To Mini USB B Cable

To convert from the AT out of the keyboard to a usb input for a modern computer to understand an active converter must be used. Thankfully others have done this before me. Soarer a user on the [deskthority](https://deskthority.net/viewtopic.php?f=7&t=2510&start=) and [geekhack](https://geekhack.org/index.php?topic=17458.0) forums has posted code for a converter.

Using the [Teensy Loader Application](https://www.pjrc.com/teensy/loader.html) I loaded Soarer's converter onto the Teesny.

Now to hook everything up!

I disassembled the case, cut the AT cable and striped the wires back.  
Then I soldered them like this :

|Keyboard OUT|Teensy|
|:----:|:----:|
|GND|GND|
|Vcc|Vcc|
|Data|D0|
|Clock|D1|

Had to be extra careful because the colors were going against convention, Black was Vcc and Red was GND in this cable. :/

<img src="/img/fujitsukeyboard6.JPG" alt="Fujitsu6" width="400"/>
<img src="/img/fujitsukeyboard8.JPG" alt="Fujitsu8" width="400"/>

To make the install cleaner I filed a square hole for my panel mount USB connector in the back. Reassembled the case.

<img src="/img/fujitsukeyboard10.JPG" alt="Fujitsu10" width="400"/>

Finally plugged in to my computer and it worked perfectly! No bugs, No oddities, just plan works on my Linux machine and just plan works on Windows too. Even the LEDs in the caps/num/scroll lock work.  Yay!  
