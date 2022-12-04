# Anti-theft system for a bike
Anti-thift system for your beloved bike.
Developed under a support of "Delft Open Hardware academy 2022".

## Motivation
- I'm a big fan of (race) biking. I'm always afraid of my bike got stolen when I park outside.
- In the Netherlands, bike thift is very common. My first bike in Delft got stolen after only two weeks of the purchese. I want to reduce unfortunate people like me.

### Ideas
The anti-theft system has two functions:
1. Prevent theft by warning sound
2. Track the bike's location in case the bike is moved (or when you just want to check that the bike is still there)

## Hardware 
- LilyGO TTGO T-Beam (v1.1 is used in this project)
![T-beam](images/T-beamv1_1.jpg)

- MPU6050
![mpu6050](images/mpu6050.jpg)

- Buzzer
![buzzer](images/buzzer.jpg)

## Instructions
### Theft attempt detection
 'detection/detection.io' contains theft attempt detection and raw GPS reading.  
 
### Lora connection
This part is developed based on [TTGO-T-Beam-Car-Tracker project by Tekk](https://github.com/tekk/TTGO-T-Beam-Car-Tracker).
The file for this task can be found under '/Lora_tracker/Lora-tracker.io'.

How to set up The Things Network (TNN) and Cayenne: (More detailed explanation may be added later) 
1. Create The Things Network account from [here](https://www.thethingsindustries.com/tts-plans/?tab=community).
2. Select your region and create a new application.
3. Insert Network Session Key, App Session Key and Device Address config.h file.
4. Register yourself for Cayenne from [here](https://accounts.mydevices.com/auth/realms/cayenne/login-actions/registration?client_id=cayenne-web-app&tab_id=hI0nUVsjSNo). 
5. In the TTN application, go to 'Payload formatters' -> select 'CayenneLPP'.
6. Select Add new -> Device/Widget -> LoRa -> The Things Network -> Cayenne LPP
7. Add Device EUI copied from TTN console to Cayenne.

### Mounting structure
CAD folder contains the file for 3D printing. 

Setting of the 3D printer: to be updated. 

## Points for future improvement
- Combine the "detection" file and "Lora-tracker" file into one file. 
- Enable switching "biking mode" (=alart sound is off) and "parking mode"(=alart sound is on).
- Improve the mounting structure. 

## License
This product is created by @nanaminh under Creative Commons BY 4.0 license.
