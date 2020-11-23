## Stenotype Machines

<img src="http://www.stenograph.com/product/image/large/45009_wave.jpg" width="300"/>

### Supported protocols

Plover supports several protocols that are in use by various machines:

* **Stentura serial**: most machines by Stenograph and many others.
* **Gemini PR serial**: typically any recent machine made by the Neutrino Group, such as the Piper, Revolution, or Infinity series.
* **ProCAT**: protocol used by all ProCAT machines.
* **TX Bolt**: an older protocol supported by some machines as a primary or secondary protocol.
* **Treal**: used only by the Treal from Word Technologies.
* **Passport**: used only by the Passport Writer from Advantage Software.

This means that, in theory, many machines work with Plover.

### Known supported stenotypes

The following machines have been confirmed by users to work with Plover
after actually trying it:

| Product Name                       | Manufacturer       | Protocol/Connection | Comments                |
| ---------------------------------- | ------------------ | ------------------- | ----------------------- |
| Elan Cybra Student                 | Stenograph         | TX Bolt (serial)    |                         |
| Flash, Blaze, Impression, and Xpression | ProCAT        | ProCAT (serial, *maybe*)             | (For Blaze and other Windows CE-based writers) USB cannot be used with Plover, it is only to transfer files created on the Blaze to your PC or CAT software. USB does not work on Windows 10, only Windows XP (with ActiveSync), and Windows Vista/7/8 with WMDC.exe (Windows Mobile Device Center). Both are abandonware. You need an RJ11 (male) to DB9 (female) to use this writer. |
| Flash Writer                       | ProCAT             | TX Bolt             | Press `Mode` (far right button), click `Setup`, then press the `Emul` button. Display should read `Emulate: Baron` |
| Gemini2                            | Neutrino Group     | Gemini PR (serial)  |                         |
| Gemini RT                          | Neutrino Group     | TX Bolt             | Must start a job on screen or in [Infinity2](http://www.infinitytraditional.com/infinity-2/) |
| Lightspeed                         | Stenovations       | TX Bolt (serial over USB/Bluetooth) | Baud rate 9600 |
| Infinity Ergonomic                 | Neutrino Group     | Gemini PR (serial over USB/Bluetooth)  | Baud rate 115200 |
| Infinity Genesis                   | Neutrino Group     | Gemini PR (serial)  |                         |
| Passport                           | Advantage Software | Passport (USB)      |                         |
| Passport Touch                     | Advantage Software | USB, Bluetooth | While in "Emulation Mode": Stentura over Bluetooth or TX Bolt over USB ﻿ |
| Protege                            | Stenograph         | Stentura (serial)   | Connect Serial-to-USB cable to serial port of Protege. Use USB jack for power only (USB drivers not avail.) [Setup Instructions](https://github.com/openstenoproject/plover/wiki/Stentura-Protege-Setup-and-Usage-Instructions)|
| Revolution Grand                   | Neutrino Group     | Gemini PR (serial)  |                         |
| Stentura 400 SRT                   | Stenograph         | Stentura (serial)   | [Setup Instructions](https://github.com/openstenoproject/plover/wiki/How-to-setup-and-use-Plover-with-a-Stentura-400SRT)  |
| Stentura 200 SRT                   | Stenograph         | Stentura (serial)   | (same instructions as the 400 SRT)  |
| Stentura 500                   | Stenograph         | Stentura (serial)   | (same instructions as the 400 SRT)  |
| Stentura 8000LX                   | Stenograph         | Stentura (serial)   | (same instructions as the 400 SRT)  |
| Tréal                              | Word technologies  | Treal (USB)         |                         |
| Wave                               | Stenograph         | Stentura (serial) OR Stenograph USB | Requires stenograph drivers to do serial on windows. All platforms can use the [plover-stenograph-usb](https://pypi.org/project/plover-stenograph-usb/0.0.3/) plugin. Make sure "serial protocol" on the Wave is set to "Stentura". |
| Luminex II                         | Stenograph         | Stenograph USB | Works with the [plover-stenograph-usb](https://pypi.org/project/plover-stenograph-usb/0.0.3/) plugin. |
