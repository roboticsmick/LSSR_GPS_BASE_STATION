# LSSR_GPS_BASE_STATION

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

Instructions:
When recording GPS coodinates for launch data. 
1. Power using a USB only (do not turn on the toggle switch).
2. Connect to PC using USB. 
3. Use the device manager to identify which COM port the GPS Base Station is connected to.

![base_station_device_manager](https://user-images.githubusercontent.com/70121687/175452873-6de6f430-a91a-487d-9fb5-e4e1b61d0b79.png)

4. Open putty (don't use the serial monitor in Arduino as it does not allow saving data and has a limited number of rows).
5. Set to serial and change the COM port to match the ID found in the device manager.

![putty](https://user-images.githubusercontent.com/70121687/175452924-882f2544-66cc-4e81-8ed4-744f0073e421.png)

6. Base stations should automaticaly pick up the GPS tracker when turned on.
7. The base station will start displaying GPS coordinates on the LCD when it has a fix.
8. SIV = Satellites in view. At least 3 should be in view to get valid data. 
9. When the rocket has landed, save the GPS coordinate data from putty as a CSV. 
10. Copy the last row of the saved data and paste it into Googlemaps. The rocket coordinates should now be available.

If the rocket coordinates were lost:
1. Unplug the USB, and turn on the GPS base station using the toggle switch.
2. Head in the direction of the last known coordinates.
3. When new coordinates are recieved by the base station, the GPS base station should update on the LCD when the rocket is detected. 
4. If you cannot see the rocket, enter the updated coordinates into your phones googlemaps, and you should be able to work out the location in the field.

