# Third-party material

## CAD and component references

The editable EasyEDA design and manufacturing files are hosted on [OSHWLab](https://oshwlab.com/keisuke054/project_agusbwba). This GitHub repository contains viewing exports and documentation. The design uses upstream symbol, footprint, and device definitions; its schematic PDF and CAD previews may reflect those definitions. The project-owned contributions' CC BY-NC-SA 4.0 license does not relicense upstream library material, supplier models, or manufacturer branding.

Component manufacturer names and part numbers identify the intended components and do not imply endorsement. Datasheets are linked rather than redistributed. The assembly preview uses simplified BMD-340 and BME688 presentation models; refer to manufacturer documentation for exact mechanical dimensions.

## Firmware

No firmware dependencies are bundled. Nordic SDK/Zephyr selection and individual sensor drivers have not been chosen. Bosch BSEC is neither included nor required by an implemented firmware image.

## PCB preview renderer

The bare-PCB artwork was rendered from the R1D Gerbers using [Gerbonara](https://github.com/jaseg/gerbonara), version 1.6.3. Gerbonara itself is not bundled; its own licensing applies to the tool.
