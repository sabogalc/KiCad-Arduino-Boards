# UNO R4 WiFi
I am not the same man I was before making this board.

As soon as I saw the 96 LED array on this board, I knew that I would be in for some work, and of all the boards in this repository, this is the only one that I am not confident would pass a fabricator's specifications. I will highlight the parts of this board that I think may be problematic below.

Firstly, the 3.3V fuse is extremely close to a GND pad on the USB-C port, which could be a possible weak point for a 3.3V short to GND to happen.

![Screenshot 2024-06-07 193424](https://github.com/sabogalc/KiCad-Arduino-Boards/assets/53708281/5d6b5edc-dffc-4a72-8393-859d5921428e)

Next of course is the placement and routing of the LEDs, especially because lots of these tracks have very little clearance between them.

![Screenshot 2024-06-07 193701](https://github.com/sabogalc/KiCad-Arduino-Boards/assets/53708281/3f5d5906-66d6-4974-b1cc-cf6c29731d31)

Some of the curved traces on this board may also be problematic, like in the example below.

![Screenshot 2024-06-07 193756](https://github.com/sabogalc/KiCad-Arduino-Boards/assets/53708281/190f2484-40ab-4c6c-a83b-6565181845d4)


All in all, if anyone does actually order the gerbers for this board, please let me know if either all is well or if there are corrections that need to be made.

Below are the screenshots of this board from KiCad's 3D board viewer.

![Screenshot 2024-06-07 191713](https://github.com/sabogalc/KiCad-Arduino-Boards/assets/53708281/55567f6d-d35f-4adf-89a3-90b4d0736346)
![Screenshot 2024-06-07 191725](https://github.com/sabogalc/KiCad-Arduino-Boards/assets/53708281/72dc5442-3d07-43a0-933c-5e52d741d0c3)