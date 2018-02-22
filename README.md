# Beetle Small Keyboards

## Overview:

Sometimes you don't need many keys for a project, and the Arduino Beetle has 10
I/O pins plus a USB port for small projects. This combination is ideal for:

    * USB based keyboards (or mice)
    * Handwired (although PCB options are possible too)
    * One to 10 keys are trivial
    * Up to 25 keys are not much harder, though a PCB would help.
    * Pogramable with macros, layers, supported by TODO: {TMK | QMK | Easy AVR} software
    * Numeric pads (often 17, 19, 21, or 22 keys)
    * Converting key "switch testers" to macro pads.
    * Simple, inexpensive hardware

## Initial project: 4 foot switches

My first project based on this technology is a foot-operated set of 4 (or 8)
switches. The plan is to support four modifier keys, to be foot-operated. They
are: Command (or Windows), Option, Control, and Shift.

The thought is that these could be used to support users with some hand problems.

This project will not require the manufacture of any printed circuit boards, 
and the switches will be hand-wired to the Beetle.

Parts count, and expenses are low.

Because the Beetle has 10 I/O pins available, and I only need 4 (or 8), I'll
(hand) wire then directly.

## Additional project

Again, with 10 I/O pins it is possible to do a standard keyboard scanning matrix
of 5 x 5 (up to 25 keys), or 4 x 6 (up to 24 keys, with a scan layout that more
closely matches the physical). These matrixes will require a diode at each
switch to prevent "ghosting."

For example, searching Amazon for: numeric pad USB, most numeric pads have 17,
to 22 keys on them, so the little Beetle will be quite capable for this
application.


## Parts list




Parts for 4 switches|Qty| Jameco  |URL
--------------------|--:|--------:|----
Adafruit Beetle     | 1 | $9.95   | [2213325](https://www.jameco.com/z/DFR0282-DFRobot-Beetle-Microcontroller-Arduino-Compatible-_2213325.html)
5 Black RCA jacks   | 2 | $1.95   | [229921](https://www.jameco.com/z/JR1625BLK-Black-Plastic-RCA-Plug-Pack-of-5-_229921.html)
4 RCA sockets (1x3")| 2 | $0.49   | [319429](https://www.jameco.com/z/CA066-Velleman-RCA-Jacks-2-Stereo-Pairs-Red-Black-Nickel-Plated_319249.html)
Case                | 1 | $4.95   | [675462](https://www.jameco.com/z/111-BK-Serpac-Electronic-Enclosures-Enclosure-Black-111-Bk-Hi-Impact-Abs-Plastic_675462.html)
USB-A to USB-micro B| 1 | $1.95   | [2196086](https://www.jameco.com/z/IFA-A104-3-Foot-USB-micro-B-Data-Sync-Charging-Cable_2196086.html)
Foot switches (4)   | 4 | $14.00   | (Tatoo, drom China)
----------------    |---|-------- | 
Estimated total     |   |$33.29   | 

### Alternate part options:

* Beetle $7.90 [Digikey](https://www.digikey.com/product-detail/en/dfrobot/DFR0282/1738-1016-ND/6588438). USB + 10 I/O; 20mm x 22mm
* 3.5 mm socket (need 4+) $0.74ea [Digikey](https://www.digikey.com/product-detail/en/cui-inc/SJ1-3523N/CP1-3523N-ND/738689)
* 3.5mm jack (need 4+) $0.84ea  [Digikey](https://www.digikey.com/product-detail/en/cui-inc/MP3-3501/CP3-1005-ND/992141)
* Case 3.6 x 2.25 x 1". Serpac 111i project box. Install RCA sockets in top. 
[digikey](https://www.digikey.com/product-detail/en/serpac/110IBK/SR110-IB-ND/95415) $4.50
* (for expanded experiments) 5v, 8 bit shift reg. $0.43 [Digikey](https://www.digikey.com/product-detail/en/texas-instruments/SN74HC164N/296-8248-5-ND/376946)



## Basic Beetle Specifications:

  Parameter | Value
  ------------------|-------------
  Microcontroller		|		ATmega32u4
  Clock Speed		|		16 MHz
  Operating Voltage		|		5V DC
  Digital I/O Pins		|		10 
  PWM Channels		|		4 
  Analog Input Channels		|		5 
  UART		|		1 
  I2C		|		1 
  Micro USB		|		1 
  Power Ports		|		2 
  Flash Memory		|		 32 KB (4KB used by bootloader)
  SRAM		|		 2.5 KB
  EEPROM		|		 1 KB
  Size          |  20x22x3.8mm


## Related / Alternate projects:

* [Mini-Emoticon-Keyboard](http://www.instructables.com/id/Mini-Emoticon-Keyboard/
) using the similar Adafruit Trinket.
* The keytee project. [GitHub](https://github.com/trebb/keytee) project. 
[Project files](https://trebb.github.io/keytee/pcb.pdf). Same processor, custom PCB.
* [Clueboard](https://clueboard.co/parts/clueboard-switch-tester) Switch Tester
Kit, or Assembled  
* NovelKeys [switch tester](https://www.novelkeys.xyz/product-category/switchtesters/)

## IO Port Mapping Beetle to Arduino Ports:
```
        
          Beetle    Digital   PWM   Analog
        Silkscreen	  Pin   Channel Channel	UART	    I2C
            RX	        0	                Serial-RX
            TX	        1	                Serial-TX
            SDA	        2	                            SDA
            SCL	        3	     3	                    SCL
            9	          9	     9	  A9		
            10	        10	  10	  A10		
            11	        11	  11	        
            A0	        A0	        A0		
            A1	        A1	        A1		
            A2	        A2	        A2		

        Power:
          Beetle
        Silkscreen	Description
            +           VCC
            -           GND
```

## Getting Started

Development resources:

* [Summary](https://deskthority.net/wiki/Easy_AVR_USB_Keyboard_Firmware) on Deskthority
* All the code and documentation on [GitHub](https://github.com/dhowland/EasyAVR/releases)


1. Plug-it in
2. Blue LED on the Beetle should flash
3. macOS:
    - Apple menu, About this Mac
    - Click System Report...
    - Select USB from the left column
    - Look for Arduine Leonardo in the USB tree
4. Windows:
    - TODO: 
    - aa

## Load the new software


Development order for Beetle experiments (Arduino-only code)
  √ reset keyboard/controller after completing task
  * Compute 4-function calculator operations (say 20 different ones) in
  *floating point*, 100, 1000, 10,000 times. Time millis them and
  report. Use random numbers?
  * 
  * Create a calculator that takes character array (string) input, treats each as a keystroke. Repeat 10,000 times. Report elapse time & result.
    * example: 123+222=345
    * 1/9*9*1000/0.5+800.765=2800.76499999998
    * Maybe use PString for display: http://arduiniana.org/libraries/PString/
  * Repeat calcs and timing with "BigNumber" -- https://github.com/nickgammon/BigNumber  
    * Mac OS X calculator seems to display and retain up to 19 digits
    * Arduino LCD display is 2 x 16 characters. (We could use more and have "guard digits")
    * Sun serial (1200 baud, start, stop) by Ben Rockwood, https://github.com/benr/SunType5_ArduinoAdapter_
      SoftwareSerial sunSerial(10, 11, true); // rxpin txpin, reverse logic (yes)

    
Using usb keyboard: https://www.pjrc.com/teensy/td_keyboard.html
Google:   arduino sending scan codes to usb keyboard


## Hardware tasks
```
2-wire Arduino to LCD project:  http://www.instructables.com/id/2-Wire-LCD-interface-for-Arduino-or-Attiny/
and again (2011): http://3g1l.com/blog-cheap-arduino-2-wire-lcd-display-0
and again (2012): https://scargill.wordpress.com/tag/2-wire-lcd-for-arduino-a-working-example/
and again:        https://playground.arduino.cc/Code/LCD3wires

Sun kbd to USB via Beetle:
  Load code, test, point Sun-only codes for F13-F24 or so. Test.  
  
keyboard.println() is broken. Space instead of \n.
scan codes instear od keyboard.print
Buffered USB for > 6 KRO
```
