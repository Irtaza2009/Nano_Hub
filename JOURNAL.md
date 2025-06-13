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
2. Also, the board would require PCBA,

so instead, I shifted to EasyEDA.

I added all the components that best fit my requirements and started wiring them, but when trying to rotate one component, I accidentally reloaded the page, so all progress was lost (learned that EasyEDA does not auto save your work the hard way) :(

Now I am downloading the desktop app and will continue with the schematic tomorrow!

**Time spent: 2 hours**

### June 13th: Almost finished the schematic!
Decided to move away from EasyEDA because all of the UI and the keyboard shortcuts were different, and I couldn't get the hang of them. So I opened up KiCAD again and again started the schematic from scratch. I used the 16-pin USB C ports schematic and, after some reasearch between FE1.1s and SL2.1A, chose FE1.1s as the USB 2.0 hub controller!

I opened up the FE1.1s datasheet and then routed each pin to where it specified. I left the config and LED pins alone for now, and will get to them later on after researching more about what they are supposed to do!

And I also routed the power pins on the hub and ports with 10uF capacitors to ground and the CC pins on the USB-C ports through 5.1kΩ resistors to ground.

<img width="951" alt="KiCAD Schematic" src="https://github.com/user-attachments/assets/8fb1fdb3-db06-4c3f-9ee7-cd841845c78b" />
