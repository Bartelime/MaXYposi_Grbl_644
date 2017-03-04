![GitHub Logo](http://www.heise.de/make/icons/make_logo.png)

Maker Media GmbH und c't, Heise Zeitschriften Verlag

***

###Grbl 1.1f2 Version for ATmega644(p) 

with multiple additions, suited for MaXYposi board (german Make: magazine, issue 2/2017). Additions by Carsten Meyer, Make Magazin Deutschland.

* 4th C axis per #define in config.h, settings configured to C360 = 1 complete turn for PNP machine or robot head @ 1/16 steps driver
* 16 Output ports for LEDs and relays, via HC595 SRs on SPI (may left unconnected)
* 32 Input ports for buttons/swiches, via HC165 SRs on SPI (may left unconnected)
* SPI transfer of realtime position data (floats), for external LCD (needs extra ATmega168/328)
* Support for dial/handwheel, direct connection to Grbl CPU. Updates machine/work position in realtime.
* Support for analog joystick with variable speed, direct connection to Grbl CPU. Updates machine/work position in realtime.
* Handwheel A/B phase on 2 port pins, must be same as LIMIT port
* Joystick on SR inputs, speed on ADC7
* Optional button panel with coordinate LCD 16x2 and up to 32 buttons, connected via SPI
* Button functions and enables defined in cpu_map.h
* M commands for additional relay switches M100/101..M106/M107 (even numbers turn on, odd turn off relays)
* Additional $I fields and build info
* New files: spi_sr.c and jogpad.c to handle SPI Rx/Tx and joystick/buttons/dial
* some additions to other filed to handle 4th axis and display/LED update

Please note ATmega644 output pin onfiguration in cpu_map.h, which heavily differs from Arduino pinout.

Put in your Arduino Sketchbook folder and select board "MaXYposi" and CPU ATmega644 or 644p.

WORK IN PROGRESS. STAY TUNED.



![GitHub Logo](https://github.com/gnea/grbl/blob/master/doc/media/Grbl%20Logo%20250px.png)

* [Licensing](https://github.com/gnea/grbl/wiki/Licensing): Grbl is free software, released under the GPLv3 license.
* For more information and help, check the Grbl **[Wiki pages!](https://github.com/gnea/grbl/wiki)**!
* Lead Developer: Sungeun "Sonny" Jeon, Ph.D. (USA) aka @chamnit
* Built on the wonderful Grbl v0.6 (2011) firmware written by Simen Svale Skogsrud (Norway).

-------------
Grbl is an open-source project and fueled by the free-time of our intrepid administrators and altruistic users. If you'd like to donate, all proceeds will be used to help fund supporting hardware and testing equipment. Thank you!

[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=CUGXJHXA36BYW)
