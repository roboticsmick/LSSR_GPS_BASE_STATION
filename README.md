# LSR_GPS_BASE_STATION

A portable, low cost GPS Rocket tracking base station. Uses a Teensy 4.1 and Ebytes LORA module to track and display the current GPS coordinates for a HPR rocket launch. Estimated range is 7km.

This was designed and built for my HPR L1 certification launch. Tracking worked perfectly and I was able to successfully monitor the launch of my rocket, then use the GPS coordinates to locate it’s landing point.

![LSR_GPS_base_station](https://user-images.githubusercontent.com/70121687/173560079-b2a9d8a2-1a8f-4d05-87ab-7fa69dd9dfa3.png)

![LSR_GPS_base_station 2](https://user-images.githubusercontent.com/70121687/173560171-f3615834-20f0-468d-95e4-4fe456b43204.png)

Parts list:
* Microcontroller – TEENSY 4.1
* RF receiver – EbyteLORA E22-900T22D (set to 915Mhz for Australia)
* GPS – UBLOX NEO_6M (also works with ATGM336H GPS Module)
* 5V Buck Converter – MPM3610 5V at 1.2A
* Compass – GY271 QMC5883 LCD – OLED 128×64
* Battery – 7.4V LIPO with XT30 connection

Version 2 will use a Raspberry Pi Pico RP2040 to bring the overall costs of the board down.

PCB design was done using Fusion 360 electronics. 

PCB printed using JLCPCB.

Case design is lasercut perspex and 3D printed. Modelled using Fusion 360.

I'm starting my 4th year of Engineering at Queensland University of Technology, Australia. Majoring in Mechatronics with the goal of being an astro roboticist, working on designs for satellites. 
