---
title: "Nano Hub"
author: "Irtaza"
description: "A custom tiny USB hub for iPad/mobile!"
created_at: "2025-06-11"
---

### June 11th: Started working on the schematic!
Opened up KiCAD and, after looking through some online references, like the onboard guide, started to place components. 
<img width="615" alt="KiCAD Schematic)" src="https://github.com/user-attachments/assets/f658ad03-0794-460a-aa73-2aa2310874b4" />

However, I soon realised that:
1. KiCAD does not have all the components that I would require in its library, and
2. Also, the board would require PCBA.

So instead, I shifted to EasyEDA.

I added all the components that best fit my requirements and started wiring them, but when trying to rotate one component, I accidentally reloaded the page, so all progress was lost (learned that EasyEDA does not auto-save your work the hard way) :(

Now I am downloading the desktop app and will continue with the schematic tomorrow!

**Time spent: 2 hours**

### June 13th: Almost finished the schematic!
Decided to move away from EasyEDA because all of the UI and the keyboard shortcuts were different, and I couldn't get the hang of them. So I opened up KiCAD again and started the schematic from scratch. I used the 16-pin USB C ports schematic and, after some research between FE1.1s and SL2.1A, chose FE1.1s as the USB 2.0 hub controller!

I opened up the FE1.1s datasheet and then routed each pin to where it specified. I left the config and LED pins alone for now, and will get to them later on after researching more about what they are supposed to do!

And I also routed the power pins on the hub and ports with 10uF capacitors to ground and the CC pins on the USB-C ports through 5.1kΩ resistors to ground.

<img width="951" alt="KiCAD Schematic" src="https://github.com/user-attachments/assets/8fb1fdb3-db06-4c3f-9ee7-cd841845c78b" />

**Time spent: 1.5 hours**

### June 14th: Finished the ports part of the schematic!
Looked at lots of USB-C hubs schematics and used them as a reference to modify my own!

- Powered each of the ports with direct 5V from the upstream USB-C.
- Added 2 decoupling capacitors on the 5V.
- Added a crystal.
- Routed the config pins using those schematics!

Also edited the resistor and capacitor values to show their actual values (e.g., 10k or 10uF) instead of "Resistor".

And routed the shields to ground.

<img width="924" alt="image" src="https://github.com/user-attachments/assets/67a6d8cc-9c48-4b66-bf04-b36a5d48d0fe" />

**Time spent: 1 hour**

### July 21st: Finished Schematic + PCB!
Finally got motivation again to work on this! I decided to scrap my KiCAD schematic and start over from scratch in EasyEDA. I also did some research and decided to replace the FE1.1S with a SL2.1A USB 2.0 hub controller!

I am going to use a USB-C port for the main IN receptacle, and then have 2 USB-C and 2 USB-A ports in the hub! And an LED to show if the connection works! 

I opened up the datasheet for the SL2.1A and got to work!

It was actually pretty fast and I think I got the schematic done within 3 hours!

<img width="1190" height="845" alt="Nano Deck Schematic" src="https://github.com/user-attachments/assets/2d741835-3673-44c7-9cd2-e9b3d6fd9913" />

Then I opened up the PCB, and arranged all of my components in a small neat square! Before routing anything, I made all the D+ and D- pins differential pairs! It helped a lot! First of all, I routed the crystal because I had learned from past experience that it should get priority placement and routing! I made sure that there were no vias on any of the D+ and D- nets! And in the end, I got away with only 2 or 3 really short vias for the 5V net, and everything else on the top layer! I didn't route the ground net this time and just made a GND plane on both layers and added some vias to connect it together!

Then, finally, I added some silkscreen art and some advanced solder mask and routing layer art!! It turned out pretty good because I had a lot of empty space left on the bottom layer for it!

<img width="448" height="354" alt="PCB top layer" src="https://github.com/user-attachments/assets/e0e40aa9-7924-46e3-b786-513cc89d4170" />
<img width="448" height="354" alt="PCB bottom layer" src="https://github.com/user-attachments/assets/7477fa74-3e11-48fa-a9af-cd6c0a658ef7" />

<img width="2160" height="1710" alt="PCB 3D Top" src="https://github.com/user-attachments/assets/ddc55475-9b6d-4600-b5af-0f99aff81550" />
<img width="2160" height="1623" alt="PCB 3D Bottom" src="https://github.com/user-attachments/assets/e99f5554-6c79-4d0d-84b7-76a6a579660f" />



