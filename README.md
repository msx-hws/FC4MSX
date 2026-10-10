# FC4MSX - MSX Floppy Disk Controller Cartridge

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](LICENSE)
[![Platform: MSX](https://img.shields.io/badge/Platform-MSX%20%2F%20MSX2%20%2F%20MSX2%2B%20%2F%20turboR-blue.svg)](#)

**FC4MSX** is an open-source Floppy Disk Controller (FDC) cartridge designed for MSX computers. It is based on and inspired by the classic **Talent TDC-600** controller design, adapted for modern retro-computing enthusiasts, homebrew makers, and engineers.

---

## ⚠️ License & Commercial Use Notice

This project is licensed under the **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)** license.

- **Non-Commercial DIY Builds:** You are free to view, download, produce PCBs for personal use, build cartridges for yourself or friends (at cost), and modify the designs under the same license terms with proper attribution.
- **Commercial Restrictions:** **Commercial production, manufacturing, or sale of PCBs, assembled cartridges, kits, or enclosures is strictly prohibited without prior written approval from the author.**
- For commercial licensing inquiries or batch manufacturing approval, please open an issue or contact the repository owner.

---

## 📖 Overview & Features

- **MSX Standard Cartridge Form Factor:** Fits standard MSX cartridge slots.
- **TDC-600 Heritage:** Uses the well-tested and highly compatible floppy disk controller architecture derived from the Talent TDC-600.
- **Drive Support:** Standard 34-pin floppy interface supporting 3.5" PC floppy drives and modern floppy drive emulators (such as **FlashFloppy / Gotek**).
- **Custom 3D-Printable Enclosure:** Snug-fit cartridge shell designed to house the PCB with cutouts for connectors and activity LEDs.
- **Open Gerber Files:** Ready-to-order manufacturing packages for PCB fab houses (JLCPCB, PCBWay, Aisler, etc.).

---

## 📁 Repository Structure

```text
fc4msx/
├── gerbers/             # Production-ready Gerber archives / drill files
├── bom/                 # Bill of Materials and component references
│   └── BOM.md
├── docs/                # Schematics, pinouts, jumper configs, flashing notes
│   ├── ASSEMBLY.md      # Step-by-step soldering & assembly guide
│   └── PINOUT.md        # Connector pinouts & drive cable configuration
├── 3d-enclosure/        # 3D printable cartridge shell (.STL & .3MF)
│   └── README.md        # Slicer recommendations and hardware assembly notes
├── LICENSE              # CC BY-NC-SA 4.0 license details
└── README.md            # This documentation
```

---

## 🛠️ Hardware Specifications & PCB Fabrication

### Ordering PCBs
You can order PCBs directly using the files in the [`gerbers/`](gerbers/) folder. Recommended fab settings:

| Parameter | Recommended Specification |
| :--- | :--- |
| **Layers** | 2 Layers |
| **PCB Thickness** | 1.6 mm (standard MSX slot thickness) |
| **Surface Finish** | HASL Lead-Free or ENIG (recommended for edge connectors) |
| **Edge Connector** | 45° Chamfer / Bevel (essential for smooth cartridge insertion) |
| **Copper Weight** | 1 oz |
| **Solder Mask** | Any color (Blue / Black / Green) |

> **Tip:** Adding gold fingers (ENIG + 45° bevel) on the MSX 50-pin edge connector significantly prolongs cartridge slot life and improves contact reliability.

---

## 🧰 Bill of Materials (BOM)

A complete list of parts, part numbers, and footprints is available in [`bom/BOM.md`](bom/BOM.md).

Primary components typically include:
- **FDC Controller IC** (e.g., Western Digital WD2793 / WD1770 / WD1772 or equivalent based on TDC-600 architecture)
- **Glue Logic / Address Decoding:** 74xx-series logic ICs (74LS/HCT family)
- **Disk ROM:** 27C256 / 28C256 or 27C128 / 27C512 EPROM/EEPROM with compatible MSX-DOS Disk ROM
- **Floppy Connector:** Standard 34-pin 2.54mm dual-row box header
- **Passives:** Electrolytic & ceramic decoupling capacitors (0.1µF), pull-up resistor networks, crystal oscillator

---

## 🖨️ 3D Enclosure Printing

The [`3d-enclosure/`](3d-enclosure/) directory contains the model files:
- **`.STL`** files for universal slicer compatibility.
- **`.3MF`** files containing pre-configured orientations and multi-part arrangements (e.g. for Bambu Studio / PrusaSlicer).

### Print Recommendations:
- **Material:** PETG or PLA+ (ABS/ASA recommended if you want heat resistance and acetone vapor smoothing).
- **Layer Height:** 0.16 mm – 0.20 mm.
- **Infill:** 20% – 30% Gyroid or Grid.
- **Walls/Perimeters:** 3 or 4 walls for rigid screw posts and connector openings.
- **Supports:** Usually not required if printed flat-face down.

---

## 🔌 Connection & Usage

1. **Floppy Cable:** Connect a standard straight or twisted 34-pin IDC ribbon cable to your 3.5" drive or Gotek emulator.
   - Refer to [`docs/PINOUT.md`](docs/PINOUT.md) for drive select jumper settings (DS0 vs DS1).
2. **Power:** Ensure power is provided to the floppy drive (5V for Gotek / standard 3.5" micro power header).
3. **Cartridge Insertion:** **Always insert or remove the cartridge while the MSX is powered OFF.**
4. **Booting:** Power on the MSX with a formatted MSX-DOS disk or Gotek image. The disk interface will initialize and present the disk prompt (`A>`).

---

## 🤝 Contributing

Feedback, bug fixes, testing notes, and improvements are welcome!
- If you build a unit, feel free to post photos in the Issues or Discussions tab.
- For modifications and pull requests, please ensure all contributions comply with the Non-Commercial ShareAlike terms.

---

## 📜 Credits & Acknowledgments

- **Talent TDC-600:** Original hardware architecture inspiration.
- **MSX Community & Resource Contributors:** Thanks to the MSX Resource Center (MSX.org) and the vintage computing community for preserving schematics, Disk ROMs, and technical documentation.
