# Belgian Digital Meter script for the P1 port
Script to parse P1 output of the Belgian electricity meter.

Prerequisites:
==============
Hardware:
- Digital Meter (Sagecom S211: Single phase, Sagecom T211-D : Three-phase and Flonidan - G4SRTV: Natural gas (as slave of the first two)
- Cable to connect to the meter (RJ11/RJ12), either serial or premade including USB to serial

Software
Either use requirements.txt:
```
pip install -r requirements.txt;
```

Or install with your package manager:
```
jensd@deb10:~$ sudo apt install python3-serial python3-crcmod python3-tabulate
Reading package lists… Done
Building dependency tree
...
Setting up python3-serial (3.4-4) ...
```

Adjustments/configuration:
==========================
At the beginning of the script, you can change the following:
- Serial port:
```
serialport = '/dev/ttyUSB0'
```
- Enable debug:
```
debug = False
```
- Add/update OBIS codes:
```
obiscodes = {}
```

More information
================
I created a blogpost where I elaborate about P1 port and data format to parse
This can be found here: https://jensd.be/1183/linux/read-data-from-the-belgian-digital-meter-through-the-p1-port
