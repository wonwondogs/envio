# Firmware development

**Status: not implemented.** There is no application source, binary, implemented USB protocol, BLE service, host utility, or proven sensor-calibration pipeline in this package.

The MCU/module is **nRF52840 / u-blox BMD-340-A-R**. Initial programming should be planned through the underside SWD pads. Do not assume that a USB bootloader has already been installed.

## Intended first implementation

- USB or Bluetooth LE transport for clearly identified sensor data.
- BME688 raw/compensated measurements with a documented heater configuration.
- OPT3001 light and LIS2DW12 acceleration readings; enable the internal pull-up for the open-drain `LIGHT_INT` input.
- PDM microphone capture with documented sampling and processing.
- A reproducible build and SWD programming procedure.

These are development goals, not completed features. SDK selection, transport formats, device identity, firmware license, and sensor calibration remain open.

## Hardware interface

See the [hardware reference](../docs/hardware.md) and [editable EasyEDA design on OSHWLab](https://oshwlab.com/keisuke054/project_agusbwba). Module-pad numbers are not nRF52840 GPIO numbers; translate them using the selected BMD-340 datasheet before writing pin configuration.

## Dependencies and open-source scope

A fully open reference implementation must account for the license and source availability of every required dependency. Bosch's BME68x Sensor API and its optional BSEC processing software are separate components. BSEC is provided under Bosch's own software terms and includes closed-source binaries; it is not bundled or selected as a required dependency here.

The first implementation can focus on documented sensor readings without claiming BSEC-derived IAQ or estimated CO₂. Any later algorithm integration must describe its own license, calibration, and limitations. See the [Bosch BME688 datasheet](https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bme688-ds000.pdf) and [Bosch software page](https://www.bosch-sensortec.com/en/software-tools/software/bme688-and-bme690-software).
