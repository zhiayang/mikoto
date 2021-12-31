# changelog

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


