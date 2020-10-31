This is a fork of the PnP-Focus project available here:

https://github.com/aruangra/PnP-Focus

Changes:
- Combine standalone PNP-Focus and PNP-Focus Stick controllers into one firmware with user configuration
- Implement proper speed control with Moonlight DRO driver compliance
- Full and half stepping 
- removed delay calls to eliminate idle and missed activities
- implemented ramped speed control for in/out movement buttons
- inplemented slowed speeds when approaching target position
- implemented motor power down after move is completed
- provided option for users to build standalone without the LCD1602 display
- created user manual documentation
- added new library of DRO ascom commands which can support dual driver commands
- added new additional display features like target position, temperature, active motor indicator, full and half step indicator
- added position count changes when switching between full and half step, so counter is valid

Removed the upload software as it makes no sense because code must be adapted to user stepper motor
I have submitted my changes to the upstream project.
Todd

The following is the original README for this project but really most of it is now obsolete by this new version.

PnP-Focus
Simplest Arduino-based focus controller

I want to share with you the Arduino-based focus controller named "PnP Focus". As the name implies, I want it to be as easy as "Plug and Play". No soldering. No hassle with firmware upload. You simply 1) buy the readily available components, 2) stack them, and 3) upload the firmware by a single click.

Features:
Manual control
LCD display
Temperature sensor
compatible with Moonlite ASCOM driver
compatible with commercially available focuser motors. such as , Robofocus, Moonlite, USB_Focus
All of them use the DB9 male connectors. 
It also works with the popular DIY stepper motors:
LSG35012F76P (12V)
28BYJ-48 (5V and 12V)
17HS13-0404S-PG27 (12V)

Components required:
Arduino Leonardo board. ($5-$10)
Ardumoto L298P motor driver board ($9). Choose the board that use Pin 3, 11, 12, 13 for driving the motor.
1602 LCD and keypad shield ($2-$10). I recommend the 1602 LCD and keypad shield by DFRobot ($10).
DS18B20 Temperature Sensor. I recommend the sensor by DFRobot ($4). 
The total cost is less than $30.

Anat


Installation:

The Original Installation approach is obsolete and not used with this version.  This V2.0 update is available in the project fork at 
Visit https://github.com/benkot/PnP-Focus 

A user manual describing the entire project, components used, user operation and operating principals is now availble at 
https://github.com/benkot/PnP-Focus/blob/master/PNP%20Focuser%20V2.0%20Documentation.pdf

Upgrades:
Users who have previously built the PNP-Focus project can simply download the new files and install the V2.0 firmware to update their previous project firmware.  Please review the provided documentation.  The whole project files are available in the PnPFocus-V2.0.zip file as a download.
https://github.com/benkot/PnP-Focus/blob/master/PnPFocus-V2.0.zip

Todd
