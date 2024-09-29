# UNO R4 Minima

## Overview
This board was very straightforward to make, and it is almost 1:1 with the factory one. Even though the UNO R4 already comes with USB-C from Arduino, the OEM footprint is one that exposes the middle plastic receptacle a bit, so I replaced it with one that has the entire port enclosed.

## Design Considerations
While working on this board, I encountered a few challenges:

- **Silkscreen Squares:** The silkscreen square etches on the left side were a bit cumbersome to design.
- **Microcontroller Routing:** Routing beneath the R7FA4M1AB3CFM#AA0 microcontroller was also relatively intricate, as seen below.

![R7FA4M1AB3CFM#AA0 Routing](https://github.com/sabogalc/KiCad-Arduino-Boards/assets/53708281/05c2723e-710b-4fbe-9f04-ec00701c5edb)

## KiCad 3D View
Below are the screenshots of this board from KiCad's 3D board viewer.
![3D View Front](https://github.com/sabogalc/KiCad-Arduino-Boards/assets/53708281/cd70726f-003e-440e-83cf-167b226f097b)
![3D View Back](https://github.com/sabogalc/KiCad-Arduino-Boards/assets/53708281/60e6f758-d43c-40a5-b40f-a17006b0a6e3)

## Real-World Application
I have successfully built this board and confirmed that it works.

![Built Board](https://github.com/user-attachments/assets/4725b076-ecb8-4943-9bd2-dba3dc088e2e)

### Important Note on Soldering
During assembly, I had to solder the buck regulator on 3 separate times since I kept blowing it up. As seen in the [ISL854102 datasheet](https://www.renesas.com/en/document/dst/isl854102-datasheet), its pin configuration is as follows:

- Pin 4: V<sub>in</sub>
- Pin 5: V<sub>out</sub>
- Pin 6: GND

![Buck Regulator Pinout](https://github.com/user-attachments/assets/8ced6c82-baca-4254-931d-bca6c51c6e46)

Naturally, shorting any one of these pins to the other can cause a detrimental short, and the 0.5mm pitch makes it easy to do so. Please be careful when soldering the buck regulator!