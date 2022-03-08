# REPORT:

# INTRODUCTION:

A fingerprint is a group of information that can be used to detect the software, network protocols, operating systems, or hardware devices.Finger print based security system can be used at many places like Industries, Offices, and Colleges or even at our home. Fingerprint sensor is the main part of this system.It is also called as Biometric sensor.User has to place his/her finger on the optical sensor part of fingerprint module.

# MAIN PURPOSE:

The main feature or specialty of fingerprint is that it is unique. It gives this project the high level security than other security systems.To operate this project first we have to enter data into the database of finger print sensor, for this we have to take impressions of fingerprints of those person whom we want to give access to our security system. This can be done once or whenever a new entry has to be added in the system. 
![Hardware Circuit](https://user-images.githubusercontent.com/71927150/157190534-b719531b-4127-47b1-afc7-7859154f80ea.jpg)


# OBJECTIVE:

The objective of this project is to construct a device that utilizes fingerprint recognition technology to allow access. It contains all neccessary  electronics to allow you to store, delete and verify fingerprints with just touch of the button.For this purpose we here use a Atmega 32 microcontroller circuit.

# SWOT ANALYSIS:
![SWOT Analysis](https://user-images.githubusercontent.com/71927150/157190563-10ae3f0a-efb5-42d9-a053-6aa7d71da92c.png)


# 4-W:

# WHAT:

 Fingerprint based security system is the most secured system as compared to other systems. Reason is that RFID card or Keys of lock can be stolen, password may be leaked. However thumbnail of every human being is unique, so lock will not open unless the same person is present to give the impression of fingerprint.
 
# WHY:

Finger Print is considered one of the safest key to lock or unlock any system as it can recognize any person uniquely and can't be copied easily.

# WHEN:

The British were impressed with Vucetich's work and in 1902 introduced fingerprinting. NSW Police quickly followed.

# WHERE:

As an example, fingerprints are used in the following fields and organizations: Law enforcement. It is used in systems for criminal IDs, such as fingerprint or palm print authentication systems. 

# 1-H

# HOW:
Fingerprint scanners work by capturing the pattern of ridges and valleys on a finger.  As a finger rests on the touch-capacitive surface, the device measures the charge; ridges exhibit a change in capacitance, while valleys produce practically no change at all. The sensor uses all this data to accurately map out prints.

# SYSTEM REQUIREMENTS:


## **HIGH LEVEL REQUIREMENTS**

| **High Level Requirements** | **Description** |
| --- | --- |
| HLR1 | Finger Print Sensor |
| --- | --- |
| HLR2 | Switches |
| HLR3 | Motor |
| HLR4 | Microcontroller |
| HLR5 | Software used |
| HLR6 | Display |

# **LOWLEVEL REQUIREMENTS**

| **Low Level Requirements** | **Description** |
| --- | --- |
| HLR1\_LLR1 | Finger Print module |
| --- | --- |
| HLR2\_LLR1 | Push Button |
| HLR4\_LLR1 | ATMEGA 328 |
| HLR5\_LLR1 | Code Blocks with AVR GCC compiler |
| HLR6\_LLR1 | SimulIDE LCD and LED |


# DESIGN:

* Here we demonstrate fingerprint based security system to authenticate users from entering particular premises.The system is useful for secure sites to provide access only to authorized users automatically. This ensures safety and security at secure sites/premises like military, navy, government as well as corporate premises.
      
* For this purpose we here use a Atmega 32 microcontroller circuit. The circuit consists of atmega microcontroller that is interfaced to fingerprint sensor, LCD display and motors to operate a door.
      
* Users are allowed to register into the system first. After registration/enrollment the system allows to start monitoring.Now if a fingerprint is detected, the system scans the fingerprint against stored ones.
      
* If a match is found, the system operates the motors to open the door for those users, else the system does not open the door.
      
* Thus we ensure a secure fingerprint authorized security system.

# LOW LEVEL DIAGRAM:

# STRUCTURAL LOW LEVEL DIAGRAM:
![Structural LLD](https://user-images.githubusercontent.com/71927150/157190619-a2ba842e-79b2-476e-83cf-f311f204a1fa.png)




# BEHAVIORAL LOW LEVEL DIAGRAM:
![Behavioural LLD](https://user-images.githubusercontent.com/71927150/157190646-8c0b8e82-9b80-4bd8-ae78-e3ca7093fbe3.png)



# HIGH LEVEL DIAGRAM:

# STRUCTURAL HIGH LEVEL DIAGRAM:
![High LLD](https://user-images.githubusercontent.com/71927150/157190682-e971c4b6-63cf-4516-83de-93955db0ea18.jpg)





# BLOCK DIAGRAM:
![Block Diagram](https://user-images.githubusercontent.com/71927150/157190707-4d8d2f58-a411-4d3c-b0bc-9a5f7b2344e8.png)

## TEST PLAN AND OUTPUT #


# Table No 1: High level test plan

|Test ID |	Description	Exp I/P	Exp O/p |
|------- |  --------------------------- |
| H_01 | Check if program is running or not.|
| H_02 | Check if circuit connection is correct or not |
| H_03 | check if running or not |
# Table No 2: Low level test plan
|Test ID |	Description	Exp I/P	Exp O/p |
|------- | ---------------------------- |
|L_01 |	Requirements showld be appropriate |
|L_02 |	Required software showld be uploaded.|
|L_03	| Should set a correct directory path |

# SOURCE CODE

We need to download some libraries. First of all we need the Adafruit Fingerprint library, the Adafruit GFX library and the Sumotoy's library for the display.

https://github.com/adafruit/Adafruit-Fingerprint-Sensor-Library

https://github.com/adafruit/Adafruit-GFX-Library

https://github.com/sumotoy/TFT_ILI9163C

#include &lt;SPI.h&gt;

#include &lt;Adafruit_GFX.h&gt;

#include &lt;TFT_ILI9163C.h&gt;

#include &lt;Adafruit_Fingerprint.h&gt;

#include &lt;SoftwareSerial.h&gt;

#include &lt;avr/pgmspace.h&gt;

void setup( void )

{

startFingerprintSensor();

display.begin();

displayLockScreen();}

void loop(){

fingerprintID = getFingerprintID();

delay(50);

if (fingerprintID ==1)

{

display.drawBitmap(30,35,icon,60,60,GREEN);

delay(2000);

displayUnlockedScreen();

displayIoanna();

delay(5000);

display.fillScreen(BLACK);

displayLockScreen();

}

if (fingerprintID ==2)

{

display.drawBitmap(30,35,icon,60,60,GREEN);

delay(2000);

displayUnlockedScreen();

displayNick();

delay(5000);

display.fillScreen(BLACK);

displayLockScreen();

}}



# OUTPUT:
