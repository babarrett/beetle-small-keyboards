# Beetle Small Keyboards

## Overview:

Sometimes you don't need many keys for a project, and the Arduino Beetle has 10
I/O pins plus a USB port for small projects. This combination is ideal for:

    * USB based keyboards
    * Handwired (although PCB options are possible too)
    * One to 10 keys are trivial
    * Up to 25 keys are not much harder.
    * Pogramable with macros, layers, supported by TODO: software
    * Numeric pads (often 17, 19, 21, or 22 keys)
    * Converting key "switch testers" to macro pads.
    * Simple, inexpensive hardware

## Initial project: 4 foot switches

My first project based on this technology is a foot-operated set of 4 (or 8)
switches. The plan is to support four modifier keys, to be foot-operated. They
are: Command (or Windows), Option, Control, and Shift.

The thought is these could be used to support users with some hand problems.

This project will not require the manufacture of any printed circuit boards, 
and the switches will be hand-wired to the Beetle.

Parts count, and expenses are low.

Because the Beetle has 10 I/O pins available, and I only need 8, I'll (hand)
wire then directly.

## Additional project

Again, with 10 I/O pins it is possible to do a standard keyboard scanning matrix
of 5 x 5 (up to 25 keys), or 4 x 6 (up to 24 keys, with a scan layout that more
closely matches the physical). These matrixes will require a diode at each
switch to prevent "ghosting."

For example, searching Amazon for: numeric pad USB, most numeric pads have 17,
to 22 keys on them, so the little Beetle will be quite capable for this 
application.


## Parts list

* 3.5 mm socket (need 4+) $0.74ea https://www.digikey.com/product-detail/en/cui-inc/SJ1-3523N/CP1-3523N-ND/738689
* 3.5mm jack (need 4+) $0.84ea  https://www.digikey.com/product-detail/en/cui-inc/MP3-3501/CP3-1005-ND/992141
* ?? Case Serpac 111i project box. Install RCA sockets in top. 
[digikey](https://www.digikey.com/product-detail/en/serpac/110IBK/SR110-IB-ND/95415) $4.50
* ?? PCB
* (for expanded experiments) 5v, 8 bit shift reg. $0.43 [Digikey](https://www.digikey.com/product-detail/en/texas-instruments/SN74HC164N/296-8248-5-ND/376946)

Beetle $7.90 [Digikey](https://www.digikey.com/product-detail/en/dfrobot/DFR0282/1738-1016-ND/6588438)
USB + 10 I/O; 20mm x 22mm



Part                |Qty| Jameco  |URL
--------------------|---|--------:|----
Adafruit Beetle     | 1 | $9.95   | [2213325](https://www.jameco.com/z/DFR0282-DFRobot-Beetle-Microcontroller-Arduino-Compatible-_2213325.html)
5 Red RCA jacks     | 2 | $1.95   | [22930](https://www.jameco.com/z/JR1625R-Red-Plastic-RCA-Plug-Pack-of-5-_229930.html)
5 Red RCA jacks     | 2 | $1.95   | [229921](https://www.jameco.com/z/JR1625BLK-Black-Plastic-RCA-Plug-Pack-of-5-_229921.html)
4 RCA sockets (1x3")| 2 | $0.49   | [319429](https://www.jameco.com/z/CA066-Velleman-RCA-Jacks-2-Stereo-Pairs-Red-Black-Nickel-Plated_319249.html)
Case                | 1 |         | [675462](https://www.jameco.com/z/111-BK-Serpac-Electronic-Enclosures-Enclosure-Black-111-Bk-Hi-Impact-Abs-Plastic_675462.html)
USB-A to USB-micro  | 1 |         | []()
Foot switch (4)     | 4 | $4.00   | 
xx                  | xx|         | 
Estimated total     | xx|         | 


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


## Resources:

* [Quick Key Adapter, 10 Button
Keyboard](http://www.instructables.com/id/Quick-Key-Adapter-10-Button-HID-
Keyboard/) PIC18F14K50. Complete parts kit: $25.00 (sold out) Programable w/Modifier keys.


CPU Board Choices:


See also: http://atmega32-avr.com/avr-comparison/

                ROM     EEROM   SRAM    I/O
    ATmega32u4  32K     1K      3.3K    26
    ATmega32u2  32K     1K      1.0K    22



## Related / Alternate projects:

[Mini-Emoticon-Keyboard](http://www.instructables.com/id/Mini-Emoticon-Keyboard/)
https://trebb.github.io/keytee/

Clueboard Switch Tester Kit Or Assembled
    https://clueboard.co/parts/clueboard-switch-tester

NovelKeys 
    https://www.novelkeys.xyz/product-category/switchtesters/
    
```
        IO Port Mapping in correspondence with Arduino Ports:
                                PWM     Analog
        Silkscreen	Digital Pin	Channel Channel	UART	    I2C
            RX	        0	                    Serial-RX
            TX	        1	                    Serial-TX
            SDA	        2	                                SDA
            SCL	        3	    3	                        SCL
            9	        9	    9	    A9		
            10	        10	    10	    A10		
            11	        11	    11	        
            A0	        A0	            A0		
            A1	        A1	            A1		
            A2	        A2	            A2		

        Power interface:
            Silkscreen	Description
            +           VCC
            -           GND
```


