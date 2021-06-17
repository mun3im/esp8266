# Scrolling Text on 8x32 LED using NodeMCU 
## Required Hardware

* NodeMCU ESP8266
* MAX7219 dot matrix
* Jumper Wires
* Breadboard (optional)

![alt text](https://maker.pro/storage/gE9cacR/gE9cacRYNOuescYwhyRkVDxiCUtGkm84VbJfOkN7.jpeg)

## MAX7219 Module Overview

There are several MAX7219 breakout boards available, two of which are more popular – one is the generic module and the other is the FC-16 module.

![max-module](https://lastminuteengineers.com/wp-content/uploads/arduino/MAX7219-Module-Variants.jpg)

![max-pinout](https://lastminuteengineers.com/wp-content/uploads/arduino/MAX7219-Dot-Matrix-LED-Display-Module-Pinout.png)

## Required Software

* Arduino IDE
* MAX72xx library (https://github.com/markruys/arduino-Max72xxPane)

## Connecting the Hardware

| LED Matrix  | ESP8266 |
| ----------- | ----|
| Vcc         | 3V  |
| GND         | G   |
| DIN         | D7  |
| CS          | D4  |
| CLK         | D5  |

## Setting Up Arduino IDE

Controlling the MAX7219 module is a bunch of work. Fortunately, MD_Parola library was written to hide away the complexities of the MAX7219 so that we can issue simple commands to control the display.

To install the library navigate to the Sketch > Include Library > Manage Libraries… Wait for Library Manager to download libraries index and update list of installed libraries.

![tools-board](https://lastminuteengineers.com/wp-content/uploads/arduino/Manage-Libraries.png)

Filter your search by typing ‘max72xx‘. There should be a couple entries. Look for MD_MAX72XX by MajicDesigns.
This MD_MAX72XX library is a hardware-specific library which handles lower-level functions. 

It needs to be paired with MD_Parola Library to create many different text animations like scrolling and sprite text effects. Install this library and it will ask you to install the MD_MAX72XX library due to the dependency.

![tools-com3](https://lastminuteengineers.com/wp-content/uploads/arduino/MD_Parola-Library-Installation.png)
