This is a fork of the PnP-Focus project available here:

https://github.com/aruangra/PnP-Focus

Changes:
Combine standalone and stick into one firmware with user configuration
-implement full and proper speed control with Moonlight DRO driver compliance
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


Removed the upload software as it makes no sense because code must be adopted to user stepper
I have submitted my changes to the upstream project.

What follows is the original README for this project.

PnP-Focus
Simplest Arduino-based focus controller

I want to share with you the Arduino-based focus controller named "PnP Focus". As the name implies, I want it to be as easy as "Plug and Play". No soldering. No hassle with firmware upload. You simply 1) buy the readily available components, 2) stack them, and 3) upload the firmware by a single click.

Features:

Manual control
LCD display
Temperature sensor
compatible with Moonlite ASCOM driver
compatible with commercially available focuser motors.
I have tested with various motors from

Robofocus
Moonlite
USB_Focus
All of them use the DB9 male connectors. It also works with the popular DIY stepper motors:
LSG35012F76P (12V)
28BYJ-48 (5V and 12V)
17HS13-0404S-PG27 (12V)
Components required:

Arduino Leonardo board. ($5-$10)
Ardumoto L298P motor driver board ($9). Choose the board that use Pin 3, 11, 12, 13 for driving the motor.
1602 LCD and keypad shield ($2-$10). I recommend the 1602 LCD and keypad shield by DFRobot ($10).
DS18B20 Temperature Sensor. I recommend the sensor by DFRobot ($4). The sensor is connected as shown in the figure below.
The total cost is less than $30.

Installation:

Visit https://github.com/aruangra/PnP-Focus , download the file "upload.zip" and unzip the file.
Then connect the micro usb cable between Arduino Leonardo and your PC.
Double click the file "upload.exe". The firmware will be uploaded to the Arduino board. And it is ready.
How to use:

You can use the ASCOM Moonlite focuser driver to control the motor.
For manual control, the keys are as follows: LEFTMOST: Save the position to EEPROM. For manual control, the position is not saved. Use this key to save the position. LEFT: Move in RIGHT: Move out UP: Backlight On/Off DOWN: Fast/Slow movement
Let me know if you have any question. Thank you.

Anat