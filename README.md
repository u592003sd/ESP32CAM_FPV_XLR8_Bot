# ESP32CAM_FPV_XLR8_Bot
Implementation of a ESP32 CAM module on a 4 wheel differential drive to record a track filled with obstacles.

## Overview:   
  This design was implemented in the XLR8 competition 2022 held at IIT Bombay by the Electronics and Robotics Club. The task at hand was to build and design drivable rovers controlled via wifi-hotspot using ESP32 and other relevant hardware. The task involved finalizing a mechanical design, then implementing a soldered electronic circuit and finally uploading a sample sketch and using an API interface to control the rover.
   
   The competition was flexible to allow new designs both mechanical and electrical to provide the user an advantage whilst naviagating the terrain. The following is our teams ideation and implementation for the challenge.
      
## Special Features:
      
      
   The ESP32 CAM is an inexpensive venture to work with cameras and use them for various tasks such as training ML models, Computer vision tasks and finds application in industry as well as rescue bots. The CAM can also be used to envision unexplored terrains.
  
   The CAM behaves like a WebServer and lacks the USB protocol on board. Thus to program the CAM module we require an FTDI adapter which has 4 primary connections namely VCC, GND, Rx and Tx. We also connect the GPIO0 pin to GND while programming the CAM module. Note to set the VCC output of the FTDI adapter at 3.3v while connecting to the ESP32 CAM for programming.
      
 #### Useful Links(reference):
 Reference Material to configure the ESP32CAM - https://dronebotworkshop.com/esp32-cam-intro/
 
 Link to the Captured FPV footage - https://drive.google.com/file/d/1GQecuxCKZNxRW80Gt-rYNZcXHTKPDTnZ/view?usp=sharing
 
## Debugging:
   We faced error which showed us that frame size was not fit and also common brownout errors but they can be resolved in the following way.
1. Either the female to female jumper cables were loose.
2. Enough power was not observed at the VCC pin.
3. The port on the laptop was not configured properly in the IDE.
