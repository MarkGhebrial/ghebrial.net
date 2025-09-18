+++
template = "page.html"
title = "BioHack RFID scanner"
+++

# BioHack rfid card scanner

As part of UCR's cybersecurity club, I designed a PCB and enclosure for an RFID reader and Raspberry Pi Pico.
It was used to check attendees into the various workshops at UCR's [2023 BioHack hackathon](https://biohack-2023.devpost.com/).

The Pi Pico's communicated with a laptop using USB serial.
A program running on the laptop read card IDs from the card reader and uploaded them to a database for counting workshop attendance.

I'm writing this page almost exactly two years after I finished this project, and I'm not in possession of any of the physical readers I built, so you'll have to excuse the lack of images.
Hopefully CAD screenshots will do.

## The PCB

The PCB schematic is nothing special; it's simply a one to one clone of the wiring on the breadboard prototype, with the addition of two status LEDs.

The board layout was a little more interesting.

The cheapo Amazon RFID readers we got were quite large (about 40mm by 60mm), and had an eight pin male header soldered on one end.
To reduce board area, I initially planned to put the Pico on the backside of the board, opposite to the RFID reader.
Eventually, I realized that there's enough space between the board and the reader to comfortably accommodate the Pico.
That meant that overall assembly could be thinner, and that the micro USB port could be right-side-up.

That revelation allowed me to make the board only barely larger than the RFID reader (the large rectangle on the silkscreen is the RFID reader's footprint):

![A screenshot of the 3D model of the PCB](/images/biohack-reader/pcb-front.png)

As you can tell, I didn't really care about silkscreen overlaps on this project.
If I were to go back in time and redo this design, I definitely would change that.

And, for good measure, here's the back of the board. The only traces on this side are for the LEDs:

![A screenshot of the 3D model of the PCB](/images/biohack-reader/pcb-back.png)

I downloaded the Raspberry Pi Pico footprint from somewhere online, I made the RFID reader footprint myself, and the LED and resistor footprints are from the KiCAD library.

## The enclosure

A bare PCB is not a very user friendly product, so I designed a compact 3D printed enclosure using Onshape.
The enclosure went through quite a few iterations before reaching the final version.

All versions of the enclosure use three M3x8mm screws which sandwich the PCB between the enclosure halves.

TODO: Finish this section.