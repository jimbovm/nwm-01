# New World Modular NWM-01 MIDI→CV Converter (hardware)

The NWM-01 is an open hardware MIDI-to-CV converter for the Eurorack format, based on the Arduino platform. It's designed to be inexpensive and easy to clone, with a low component count and all components cheap to buy in multiples from your favourite supplier. It begun as an experiment around just how far a simple set of inexpensive components could be pushed.

It's truly open source, with KiCad project files and source code for the firmware available under permissive licences. This repository's files are for the hardware only. For the firmware, see [the nwm-01-firmware repository](https://github.com/jimbovm/nwm-01-firmware).

*⚠ The KiCad project for the motherboard has been removed while I redesign it around an Arduino Nano. The first design used a discrete ATMEGA328-P with the Arduino firmware, but I was dissatisfied with it.*

## Bill of materials

A number of components are optional or not required for certain configurations, which can lower the cost of construction. See the footnotes for details. 

### Semiconductors etc.

* 1 × Arduino Nano or clone microcontroller board
* 1 × 7805 linear 5V voltage regulator[^1]
* 1 × 6N139 opto-isolator
* 1 × 1N4148 diode
* 1 × 28-pin narrow DIP socket[^2]
* 1 × 8-pin DIP socket[^2]

### Capacitors

* 1 × 100nF capacitor
* 3 × 10µF electrolytic capacitors[^3]

### Resistors

* 1 × 220Ω resistor
* 1 × 470KΩ resistor
* 2 × 10KΩ resistor

### Connectors

* 1 × panel mount 5-pin DIN connector
* 5 × female mono minijack (3.5mm TS) connectors
* 2 × 7-pin female header[^4]
* 1 × 3-pin female header[^5]
* 1 × 4-pin male header[^6]
* 1 × 3-pin male header[^7]
* 2 × 15-pin female header
* 3 × header shunts[^8]
* 1 × 10-pin **or** 16-pin IDC header[^9]

### Hardware

* 2 × M3 screws (PC case screws work fine)
* 2 × M3 standoffs. How long these need to be depends on various factors such as what kind of minijacks you are using and if you are using female headers for the front panel wiring. 30mm should be an acceptable size, but do your own measurements.
* 2 × M3 nuts (or another 2 × M3 screws if your standoffs have holes at both ends)
* 2 × M3 or M4 nuts with bolts

[^1]: Optional, omit if you have and want to use a 5V supply from your bus.

[^2]: Socketing the chips is recommended but by definition not required.

[^3]: Only 2 10µF capacitors are required if the 7805 is omitted.

[^4]: Optional, omit if you don't mind hard-wiring the front panel jacks.

[^5]: Optional, omit if you don't mind hard-wiring the front panel MIDI socket.

[^6]: Optional, omit if you don't want selectable routing of CV and gate outputs to the 16-pin bus.

[^7]: Optional, omit if not using the 7805 or if you don't want selectable internal and external 5V.

[^8]: 2 for the CV/gate to bus header, 1 for the 5V selector header, only as many as needed for the above headers are required.

[^9]: A 16-pin connector is required if routing CV and gate to the bus is desired, otherwise a 10-pin connector is fine. While a shrouded IDC header connector is electrically more optimal, at least in theory, two rows of 5 or 8 header pins can be substituted.

In addition to the above you will need a quantity of wire for hooking up the front panel to the main board. I recommend 0.6mm wire in a variety of colours, but use what you like.

### Legal

This hardware, including the firmware source code, is released under the terms of the CERN Open Hardware Licence Version 2 — Permissive, an [Open Source Initiative-approved licence](https://opensource.org/license/cern-ohl-p).

That means you can do practically anything with this design. That applies whether you are a solitary maker or a Chinese factory that wants to mass-produce it, because I designed it in the hope that it would be useful to electronic musicians, not to make money.

### About New World Modular

New World Modular is a project to produce open source, low cost, easily cloneable utility modules for the Eurorack modular synthesizer format that can be built with a small subset of components 
