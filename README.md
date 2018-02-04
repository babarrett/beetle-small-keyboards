# foot-switch

With thoughts of support for users with some hand problems.

by Bruce Barrett

## Parts list

* 3.5 mm socket (need 4+) $0.74ea https://www.digikey.com/product-detail/en/cui-inc/SJ1-3523N/CP1-3523N-ND/738689
* 3.5mm jack (need 4+) $0.84ea  https://www.digikey.com/product-detail/en/cui-inc/MP3-3501/CP3-1005-ND/992141
* ?? Case Serpac 111i project box. Install RCA sockets in top. 
[digikey](https://www.digikey.com/product-detail/en/serpac/110IBK/SR110-IB-ND/95415) $4.50
* ?? PCB
* (not needed) 5v, 8 bit shift reg. $0.43 https://www.digikey.com/product-detail/en/texas-instruments/SN74HC164N/296-8248-5-ND/376946

Beetle $7.90 [Digikey](https://www.digikey.com/product-detail/en/dfrobot/DFR0282/1738-1016-ND/6588438)
USB + 10 I/O; 20mm x 22mm

http://www.instructables.com/id/Mini-Emoticon-Keyboard/


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



Part                |Qty| Jameco | 
--------------------|---|--------|--------:|--------|---------
Adafruit Beetle     | 1 |      | $7.90   |
5 RCA jacks         | 1 |      | $1.95   |
4 RCA sockets (1x3")| 1 |      | $0.49   |
Case                | 1 |
USB-A to USB=B      | 1 |
Foot switch (4)     | 4 |      | $4.00   |
 | xx | | | | |
Estimated total     | xx  |    |



## Resources:

* [Quick Key Adapter, 10 Button
Keyboard](http://www.instructables.com/id/Quick-Key-Adapter-10-Button-HID-
Keyboard/) PIC18F14K50. Complete parts kit: $25.00 (sold out) Programable w/Modifier keys.


CPU Board Choices:


Part                            |CPU        |I/O | Mhz | Size        |   Notes
--------------------------------|-----------|---:|----:|-------------|---------
Beetle 1738-1016-ND             |ATmega32u4 | 10 |16   | 20x22x3.8mm | Arduino Leonardo
µduino ($18, 15-March)          |ATmega32u4 | 20 |16   | 12x12mm     |
KeyTee (open-source)            |ATmega32u2 | 20 |16   | 12x12mm     |


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
                






