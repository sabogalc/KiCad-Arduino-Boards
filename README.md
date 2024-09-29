# KiCad Arduino Boards

## Introduction
This repository contains KiCad version 8 design files for eight different Arduino boards that have been recreated from scratch. I was first inspired to work on this project when I received an Arduino Uno R3 for a class project (which you can read [here](https://github.com/sabogalc/KiCad-Arduino-Boards/blob/main/Remote%20Temperature%20Monitoring%20Project.pdf)). Although I had never used an Arduino before, I found it quite useful and versatile. However, I wanted to make some changes to better suit my needs.

## Project Motivation
While working with the Arduino Uno R3, I was frustrated by the need for a USB-B printer cable to use it. Since the Arduino hardware is open source, I decided to recreate the board with a USB-C connector. Additionally, I learned that Arduino boards are not made in KiCad, so I figured this project could also have another benefit in making the designs more open and accessible. Although buying an R4 Minima that already comes with USB-C would have been easier and less expensive, I enjoyed the challenge of re-designing the board myself.

## Design Process
Every Adruino board I could find is made in either EAGLE or Altium, and KiCad has importers for both of these formats. However, importing designs always comes with a level of artifacting and other inaccuracies. The effort to correct the imports would be comparable to remaking the board from scratch, so I opted for the latter since it would produce a cleaner end result. 

Given the popularity and open-source nature of Arduino boards, I assumed that partial or complete KiCad versions might already exist. The following repositories were helpful for getting started:
- [Arduino Uno R3 From Scratch](https://github.com/rheingoldheavy/arduino_uno_r3_from_scratch): Schematic and BOM
- [Arduino Uno KiCad Template](https://github.com/Jeff-Russ/Arduino_Uno_Template): Bare board layout
- [Arduino UNO R3 BOM](https://gist.github.com/yahyatawil/ee6ad731bcf5a5b37dcf2cac04245fbe): BOM only

Even with these resources, I had to find a reset switch footprint myself, but eventually I landed on a compatible one with the TS06-667-30-BK-100-G-SMT-TR by CUI Devices. I now had every piece I needed to make a schematic and PCB, and while doing the PCB layout I would consistently reference the imported design and try to make the component placement and routing as close to the original as possible.

## Visual Comparison
Below is a comparison of the imported UNO R3 board and my completed board, highlighting the differences and benefits in re-making the board from scratch. The most apparent differences are in the silkscreen labeling and the included 3D models of the components:

![Comparison Image](https://github.com/sabogalc/KiCad-Arduino-Boards/assets/53708281/d2d07999-eb65-429c-b417-9989f5a76a95)

## Boards Included
This repository includes designs for:
- Arduino Uno R3
- Arduino Uno R3 SMD
- Arduino Uno R4 Minima
- Arduino Uno R4 WiFi (this one may have some issues; see its folder for details)
- Arduino Leonardo
- Arduino Micro
- Arduino Nano
- Arduino Mega 2560

For details about each board, refer to the `README` file in their respective folders.