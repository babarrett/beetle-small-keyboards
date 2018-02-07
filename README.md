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

Because the Beetle has 10 I/O pins available, and I only need 8, I'll (hand)
wire then directly.

## Additional project

Again, with 10 I/O pins it is possible to do a standard keyboard scanning matrix
of 5 x 5 (up to 25 keys), or 4 x 6 (up to 24 keys, with a scan layout that more
closely matches the physical). These matrixes will require a diode at each
switch to prevent "ghosting."

For example, searching Amazon for: numeric pad USB, most numeric pads have 17,
18, 19, 20, 21, or 22 keys on them, so the little Beetle will be quite capable
for this application.


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


## Parts list

* 3.5 mm socket (need 4+) $0.74ea https://www.digikey.com/product-detail/en/cui-inc/SJ1-3523N/CP1-3523N-ND/738689
* 3.5mm jack (need 4+) $0.84ea  https://www.digikey.com/product-detail/en/cui-inc/MP3-3501/CP3-1005-ND/992141
* ?? Case Serpac 111i project box. Install RCA sockets in top. 
[digikey](https://www.digikey.com/product-detail/en/serpac/110IBK/SR110-IB-ND/95415) $4.50
* ?? PCB
* (not needed) 5v, 8 bit shift reg. $0.43 https://www.digikey.com/product-detail/en/texas-instruments/SN74HC164N/296-8248-5-ND/376946

Beetle $7.90 [Digikey](https://www.digikey.com/product-detail/en/dfrobot/DFR0282/1738-1016-ND/6588438)
USB + 10 I/O; 20mm x 22mm



Part                |Qty| Jameco | Digikey | Mouser | other?
--------------------|---|--------|--------:|--------|---------
Adafruit Beetle     | 1 |      | $7.90   |
3.5 mm jack (4)     | 4 |      | $0.74   |
3.5mm socket (4)    | 4 |      | $0.84   |
Case                | 1 |
USB-A to USB=B      | 1 |
Foot switch (4)     | 4 |      | $4.00   |
 | xx | | | | |
Estimated total     | xx  |    |



Part                |Qty| Jameco |          |
--------------------|---|--------|--------:|
Adafruit Beetle     | 1 |        | $7.90   |
5 RCA jacks         | 1 |        | $1.95   |
4 RCA sockets (1x3")| 1 |        | $0.49   |
Case                | 1 |        |     |
USB-A to USB=B      | 1 |       |           |
Foot switch (4)     | 4 |      | $4.00   |
xx                  | xx|      |       |
Estimated total     | xx|        |          |



## Resources:

* [Quick Key Adapter, 10 Button
Keyboard](http://www.instructables.com/id/Quick-Key-Adapter-10-Button-HID-
Keyboard/) PIC18F14K50. Complete parts kit: $25.00 (sold out) Programable w/Modifier keys.


CPU Board Choices:


Part                            |CPU        |I/O | Mhz | Size        |   Notes
--------------------------------|-----------|---:|----:|-------------|---------
Beetle 1738-1016-ND             |ATmega32u4 | 10 |16   | 20x22x3.8mm | Arduino Leonardo
µduino ($18, 15-March)          |ATmega32u4 | 20 |16   | 12x12mm     |
KeyTee (open-source)            |ATmega32u2 | 20 |16   | ?mm     |
Mega32u2_v2 (open-source)       |ATmega32u2 | 19 |16   | 19.05x19.05mm |  $2.85 at OSHpark + components. USB


See also: http://atmega32-avr.com/avr-comparison/

                ROM     EEROM   SRAM    I/O
    ATmega32u4  32K     1K      3.3K    26
    ATmega32u2  32K     1K      1.0K    22


    Beetle:
        Flash Memory: 32 KB of which 4 KB used by bootloader
        SRAM: 2.5 KB
        EEPROM: 1 KB

    uduino: https://www.crowdsupply.com/uduino/uduino
        Flash Memory: 28 KB available for programming, 4 KB for the bootloader
        
    KeyTee: https://github.com/trebb/keyteehttps://github.com/trebb/keytee
                

## Related projects:

[Mini-Emoticon-Keyboard](http://www.instructables.com/id/Mini-Emoticon-Keyboard/)
https://trebb.github.io/keytee/





