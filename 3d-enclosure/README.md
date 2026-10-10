# FC4MSX 3D Enclosure

This folder contains the 3D-printable enclosure files for the FC4MSX cartridge.

## File Inventory
- `.STL` files: Universal 3D mesh files compatible with any slicer (Cura, PrusaSlicer, OrcaSlicer, Bambu Studio, etc.).
- `.3MF` files: Project files containing recommended print orientation, wall thickness, infill patterns, and support boundaries.

## Recommended Print Settings
| Parameter | Setting |
| :--- | :--- |
| **Material** | PLA+, PETG, or ABS/ASA |
| **Layer Height** | 0.16 mm - 0.20 mm |
| **Walls / Perimeters** | 3 to 4 walls (for solid screw standoffs) |
| **Top / Bottom Layers** | 4-5 layers |
| **Infill** | 20% - 30% (Gyroid or Grid) |
| **Supports** | Usually not required when placing outer faces flat on the print bed |

## Assembly Instructions
1. Place the populated PCB into the bottom shell half, aligning the MSX edge connector with the front opening.
2. Route any external headers / 34-pin floppy ribbon cables through the designated cutout.
3. Fit the top shell half over the PCB.
4. Fasten using M2 or M2.5 screws (do not overtighten into plastic bosses; if using threaded brass heat-set inserts, press them in prior to assembly).
