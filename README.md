## みこと

nRF52840 microcontroller, in a pro-micro footprint, inspired by the [nrfMicro](https://github.com/joric/nrfmicro) and [nice!nano](https://nicekeyboards.com/nice-nano).

### what

1. VDDH power path (5V USB power, and/or 3.7V Li-ion battery)
2. software controllable battery charge current (off, ~100mA, ~250mA, ~350mA)
3. ESD protection on USB lines, and 500mA fuse protection for VBUS and EXT_5V
4. "Bidirectional" power over EXT_5V

Note that the project files use kicad nightly (5.99).

### ext_5v

The EXT_5V pin acts both as a power input and a power output; normally it is an input. When VBUS is high (ie. USB is connected), it will output VBUS (minus a schottky drop, ~0.3V).

EXT_5V is connected to the battery charger, so if you wire your TRRS (for split keyboards) to it (instead of a 3.3V VCC line), you can charge the battery on both halves by only plugging in one half to USB.


### assembly

All components are 0402 (1005 metric) or larger, and can be placed by hand without magnification (assuming you are good enough :D). A stencil is mandatory --- get a 100µm (0.1mm) thick stencil.

<center><img src="./misc/rev-5.14.png" width="300px"></center>

From rev 5 onwards, mikoto is no longer optimised for JLCPCB SMT service. There are still LCSC part numbers (because I still buy the parts from LCSC), but those might not be available on JLC. Also note that the "wings/tabs" are removed, so you need to modify the board so it meets the minimum 20mm width.

It would probably be a good idea to get an electropolished stencil; I can't get two prints a row to succeed without completely cleaning the stencil after the first print.

There's no "component silkscreen" on the board except 4 lines to align the nRF chip, so using something like KiCad's [Interactive BOM](https://github.com/openscopeproject/InteractiveHtmlBom) plugin is a good idea.

### problems

For now, there are no problems inherent with the design, although I personally have yet to produce a board without any issues --- all related to GPIOs not being connected properly.

Notably, the radio works correctly, and antenna performance is quite improved from revision 4.

### license

Licensed under the Apache 2.0 license, see [LICENSE](./LICENSE).

If you encounter any problems, feel free to open an issue on this repo. However, I am *not obligated* to provide any support, and you undertake any assembly/manufacturing/purchasing **at your own risk**.

> on an **AS IS** BASIS, **WITHOUT WARRANTIES** OR CONDITIONS OF ANY KIND, either express or implied, including, without limitation, any warranties or conditions of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A PARTICULAR PURPOSE.

> In **no event** and under no legal theory, ..., shall any Contributor be liable to You for damages, including any direct, indirect, special, incidental, or consequential damages of any character arising as a result of this License or out of the use or inability to use the Work.

