## みこと

nRF52840 microcontroller, in a pro-micro footprint, inspired by [nrfMicro](https://github.com/joric/nrfmicro) and [nice!nano](https://nicekeyboards.com/nice-nano).

### what

1. VDDH power path (5V USB power, and/or 3.7V Li-ion battery)
2. designed for split keyboards, sending 4.5V (via `EXT_5V`) over the TRRS
3. supports charging the secondary half from the USB-connected half for splits

Note that the project files use kicad nightly (5.99).


### assembly

Currently, only revision 4.7 has been assembled with JLC's SMT service. Specs:

- 4 layer board, 1.6mm
- ENIG plating
- impedance controlled, 7628 stackup

Everything else should be standard. ENIG is used because HASL might be too uneven for the weird aQFN footprint (basically an LGA) of the nRF52840.

Revision 4.7, assembled at JLCPCB (June 2021):

![rev-4.7](misc/rev-4.7.png)

No support will be provided for any problems faced if you decide to order and/or assemble a PCB.


### problems:

#### rev 4.7
1. battery power path is completely broken, don't use it
2. both LEDs are way too bright, with 1k resistors
3. antenna needs tuning, but this has to wait; it isn't that bad for now
4. missing a ground pad on the back (along with the `VDD` pad) for SWD programming
5. schottky diode (power path) may or may not overheat...

Regarding the antenna: performance seems similar to the nice!nano, but I think it could be better with proper tuning.



### license

Licensed under the Apache 2.0 license, see [LICENSE](./LICENSE). Importantly, there is NO SUPPORT PROVIDED, IN ANY FORM, for this project. Order/print/assemble/whatever at your own risk.
