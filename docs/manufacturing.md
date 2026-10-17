# Manufacturing notes

## Reference configuration

| Item | Current design |
| --- | --- |
| Revision | R1D single board |
| PCB dimensions | Approximately 46.48 × 17.5 mm |
| Copper layers | 4 |
| Nominal board thickness | 1.6 mm |
| Preview solder mask | Black; select the desired mask color separately in the fabrication order |
| Design stack reference | JLC04161H-7628 |
| Assembly | Both sides, 18 placements: 7 top / 11 bottom |
| BOM groups | 11 |

Download the R1D Gerber ZIP and matching BOM/CPL from the [OSHWLab project attachments](https://oshwlab.com/keisuke054/project_agusbwba). The Gerber ZIP and accompanying BOM/CPL belong together. The native design still needs manufacturing and electrical review; do not replace a four-layer design with a two-layer order setting.

## Assembly preparation

1. Select a single-board order. There is one sensor circuit per board; this package contains no multi-up sensor panel.
2. Upload the R1D Gerber and matching JLCPCB BOM/CPL.
3. Have the assembler confirm support rails/fiducials and separation around the USB-A connector.
4. Recheck the exact BOM parts, stock availability, side, rotation, and position. The original stock snapshot is historical and is not a current stock guarantee.
5. Confirm microphone handling, the 0.60 mm sound hole, sensor exposure, and applicable no-clean assembly requirements with the assembler.
6. Review the final DFM and assembly preview before submitting an order.

The selected U1 is **BMD-340-A-R** despite the library footprint's BMD-341 name. Manufacturing footprints and library model shapes should be compared against the selected supplier parts. Never infer a substitution solely from a matching 3D model.

## Still to verify

- Automatic rails, USB-plug overhang, board separation, and final dimensions.
- USB signal geometry and return reference on the actual manufactured stack.
- RF behavior and sensor exposure in the intended enclosure.
- BOM/CPL import acceptance, component orientation, and assembly quality.
- Power-up, firmware programming, and sensor operation on an assembled board.

DRC results are design checks, not evidence of a working assembled sensor. Fabrication and assembly have not been confirmed by this preparation package.
