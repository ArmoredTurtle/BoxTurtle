# BoxTurtle V1.0
BoxTurtle Automated Filament Changer (requires AFC-Klipper-Add-On (Alpha))

![BT_Render](https://github.com/user-attachments/assets/c06e961f-8d1d-41ae-9c80-036669ba2657)

BoxTurtle is exactly what it appears to be -- an open source AMS style filament changer for [Klipper](https://klipper3d.org) machines. 
The goal of BoxTurtle is to deliver a user experience as close to an AMS as possible in vanilla Klipper. i.e. an "AMS" for any klipperized printer regardless of form factor but [VORON Design](https://vorondesign.com) printers in particular.
BoxTurtle requires the use of the AFC-Klipper Add-On (found [here](https://github.com/ArmoredTurtle/AFC-Klipper-Add-On)).

If you appreciate the work we are doing, you can support us [here](https://www.armoredturtle.com/pages/donate).

# How it works
Box Turtle is a lane-based Automated Filament Changing (AFC) system, referred to as "Type B MMU" by some.
This means that each "lane" has its own motor responsible for moving filament to and from the tool head. This system uses no selector cart and no servos. Each lane motor syncs with the toolhead once the filament activates a filament sensor (such as [FilaTector](https://github.com/ArmoredTurtle/Filatector)) in (or near) the toolhead.
In order to cover any discrepancies in rotation distance between the toolhead's extruder and lane motors rotation distance, a toolhead buffer like [Belay by Annex Engineering](https://github.com/Annex-Engineering/Belay) or [TurtleNeck](https://github.com/ArmoredTurtle/TurtleNeck) by ArmoredTurtle is used.
This is a "bufferless" (no spaghetti boxes) system akin to the AMS. Each lane has its own independant respooler that uses a brushed motor to rewind the spool, and to assist the lane motor in feeding to prevent spools bucking out and/or tangling.
To enable pwm brushed motor control, BoxTurtle requires a "custom" MCU made by [Isik's Tech @xbst](https://github.com/xbst/AFC-Lite/) called AFC-lite.
BTT MMB CAN support for BoxTurtle will not be permanent as it is a bandaid solution for testing BoxTurtle on a broader scale more quickly. 

