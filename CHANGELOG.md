# changelog

Note that numbers are skipped arbitrarily based on my whims and fancies.



## revision 6.3

Previous revision: 6.1

Compatibility:

- (Slightly) incompatible pinout: `VDDH` pin (top right) changed to `VDD`
- Stencil / position / parts compatible with 5.17+
- Underside pads compatible with 6.1

Changes:

1. Change the `VDDH` extra pin to be `VDD` instead; note that it's usually an output, and should only draw a maximum of 25mA (less when transmitting!)
2. Fiddle slightly with the antenna layout (with ref. to the nRF52840 Dongle from Nordic) even though I don't know what I'm doing
3. Adjust trace routing around the antenna feed to improve ground plane coverage



## revision 6.1

Previous revision: 5.20

Compatibility:

- Incompatible pinout, bottom pad layout for USB changed (SWD pad positions unchanged).
- Stencil / position / parts compatible with revisions 5.17 - 5.20.

Changes:

1. Changed `P1.00` to `P1.08` (still high drive)
2. Exposed the old `P1.00` as an `SWO` pad instead (useful for debug trace output)
3. Changed the `VBUS` pin to expose `VDDH` instead
4. `VBUS` exposed as an underside pad


