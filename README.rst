ESP32-NESEMU, a Nintendo Entertainment System emulator for the ESP32
====================================================================

This is a quick and dirty port of Nofrendo, a Nintendo Entertainment System emulator. It has basic sound support, but can emulate a NES at close to full speed, albeit with some framedrop due to the way the display is driven.

Warning
-------

This is a proof-of-concept and not an official application note. As such, this code is entirely unsupported by Espressif.


Compiling
---------

This code is an esp-idf project. You will need esp-idf to compile it. Newer versions of esp-idf may introduce incompatibilities with this code;
for your reference. esp-idf test work well version: v3.3.4

Controller
----------

This emulator fully supports the Faces Gamepad kit: https://m5stack.com/collections/all/products/face

ROM
---
If you want to use your own, please remember official nintendo roms are under copyright and the user bears the responsibility for any legal action.

Use esptool to flash the files to the device:

``esptool.py --chip esp32 write_flash -fs 4MB 0x100000 <rom-file.nes>``

Copyright
---------

Code in this repository is Copyright (C) 2016 Espressif Systems, licensed under the Apache License 2.0 as described in the file LICENSE. Code in the
components/nofrendo is Copyright (c) 1998-2000 Matthew Conte (matt@conte.com) and licensed under the GPLv2.

