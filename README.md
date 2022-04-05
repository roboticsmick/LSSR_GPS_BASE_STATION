# LSR_GPS_BASE_STATION

A portable field rocket tracking base station that uses GPS and compass data to track and retrieve HPR rockets via LORA communication.

![image](https://user-images.githubusercontent.com/70121687/161655242-17823f1e-89f4-4d46-a6a2-5ff1fd24670a.png)

Hardware:

* TEENSY 4.1
* EBYTE LORA E22-900T22D (set to 915Mhz for Australian usage)
* UBLOX NEO 6M GPS
* MPM3610 5V 1.2A
* GY271 QMC5883 COMPASS
* OLED LCD 128x64
* 7.4V LIPO WITH XT30 CONNECTION
* C++ (platformIO)

Software will be open-source, but is currently a work in progress. I am hoping I can implment the RadioLib library (https://github.com/jgromes/RadioLib) with the Teensy.

Case design will also be shared, but needs a few more refinements to better secure the antenna bracket.

All PCB design and modelling was done using Fusion360. The board and schematic files were saved for Eagle 9.X compatibility in the hopes that would make the files more accessible?

I'm just starting my 4th year of Engineering at Queensland University of Technology, Australia. Majoring in Mechatronics with the goal of working on PCB design for satellites. 
