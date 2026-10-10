# FC4MSX - MSX Floppy Disk Controller Cartridge

[![Platform: MSX](https://img.shields.io/badge/Platform-MSX%20%2F%20MSX2%20%2F%20MSX2%2B%20%2F%20turboR-blue.svg)](#)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)#license--commercial-use-notice)

**FC4MSX** is a Floppy Disk Controller (FDC) cartridge designed for MSX computers. It is based on and inspired by the classic **Talent TDC-600** controller design, adapted for retro-computing enthusiasts, homebrew makers, and engineers who want to build their own cartridge.

---

## 📸 Hardware Previews

| 3D Isometric View | Top View (Components) | Bottom View |
| :---: | :---: | :---: |
| ![FC4MSX 3D View](images/pcb-3d.png) | ![FC4MSX Top View](images/pcb-top.png) | ![FC4MSX Bottom View](images/pcb-bottom.png) |

*(Cartridge enclosure files and instructions are located in [`3d-enclosure/`](3d-enclosure/)).*

---

## 📖 Overview & Features

- **MSX Standard Cartridge Form Factor:** Fits directly into standard MSX, MSX2, MSX2+, and turboR cartridge slots.
- **TDC-600 Heritage:** Implements the compatible floppy disk controller architecture derived from the Talent TDC-600.
- **Drive Support:** Standard 34-pin floppy interface supporting 3.5" PC floppy drives and modern floppy emulators (such as **FlashFloppy / Gotek**).
- **Custom 3D-Printable Enclosure:** Snug-fit cartridge shell designed to house the PCB with cutouts for connectors and activity LEDs.
- **Ready-to-Order Gerbers:** Complete manufacturing package for standard PCB fab houses (JLCPCB, PCBWay, Aisler, etc.).

---

## 🛠️ Hardware Specifications & PCB Fabrication

### Ordering PCBs
You can order PCBs directly using the ready-to-upload archive in [`gerbers/`](gerbers/):
👉 **[`gerbers/FC4MSX-Gerbers-v1.0.3.zip`](gerbers/FC4MSX-Gerbers-v1.0.3.zip)**

| Parameter | Recommended Specification |
| :--- | :--- |
| **Layers** | 2 Layers |
| **PCB Thickness** | 1.6 mm (standard MSX slot thickness) |
| **Surface Finish** | **ENIG (Immersion Gold)** strongly recommended for cartridge edge connector wear resistance |
| **Edge Connector** | **45° Chamfer / Bevel** (essential for smooth insertion and preserving slot pins) |
| **Copper Weight** | 1 oz |
| **Solder Mask** | Any color |

---

## 🧰 Bill of Materials (BOM)

- **Interactive BOM:** Open [**`bom/ibom.html`**](bom/ibom.html) in your browser for a visual component locator and interactive assembly checklist.
- **Detailed Reference:** See [`bom/BOM.md`](bom/BOM.md) for individual component footprints and notes.

### Key ICs & Components
| Reference | Component | Description / Package |
| :--- | :--- | :--- |
| **U1** | **WD37C65** | Floppy Disk Controller (DIP-40) |
| **U2** | **74LS04** | Hex Inverter (DIP-14) |
| **U3** | **74LS138** | 3-to-8 Line Decoder (DIP-16) |
| **U4** | **W27C512** | 64K EEPROM (DIP-28) with TDC-600 compatible MSX-DOS Disk ROM |
| **Y1** | **16 MHz** | Crystal Oscillator (DIP-8) |
| **J1** | **MSX Slot** | 50-Pin MSX Cartridge Edge Connector (PCB Gold Fingers) |
| **J2** | **FDD Header** | Standard 34-Pin (2x17) boxed shrouded header (2.54mm pitch) |
| **C1–C5** | **100nF (0.1µF)** | Ceramic decoupling capacitors |
| **C6** | **22µF** | Radial electrolytic filter capacitor (16V+) |
| **R1–R4** | **150 Ω** | 1/4W axial resistors |
| **R5** | **1 kΩ** | 1/4W axial resistor |
| **JP1–JP4** | **Solder Jumpers** | 3-pad SMD solder jumpers |

---

## 🖨️ 3D Enclosure Printing

The [`3d-enclosure/`](3d-enclosure/) directory contains the shell model files:
- [**`FC4MSX-bottom.stl`**](3d-enclosure/FC4MSX-bottom.stl) — Lower shell half with mounting posts and slot guides.
- [**`FC4MSX-top.stl`**](3d-enclosure/FC4MSX-top.stl) — Upper shell half with opening for the 34-pin floppy header.
- [**`FC4MSX.3mf`**](3d-enclosure/FC4MSX.3mf) — Pre-arranged project file with recommended print settings.

### Print Recommendations:
- **Material:** PETG or PLA+ (ABS/ASA for higher thermal endurance).
- **Layer Height:** 0.16 mm – 0.20 mm.
- **Walls/Perimeters:** 3 or 4 walls for sturdy screw bosses and connector edges.
- **Infill:** 20% – 30% Gyroid or Grid.
- **Supports:** Not required when placing flat outer faces down onto the print bed.

---

## 🔌 Connection & Usage

1. **Floppy Cable:** Connect a standard 34-pin IDC ribbon cable to your 3.5" drive or Gotek emulator.
   - Refer to [`docs/PINOUT.md`](docs/PINOUT.md) for drive select jumper notes (DS0 vs DS1).
2. **Drive Power:** Ensure external power is supplied to the floppy drive (5V for Gotek / standard floppy power connector).
3. **Cartridge Insertion:** **Always insert or remove the cartridge while the MSX computer is powered OFF.**
4. **Booting:** Power on the MSX with a formatted MSX-DOS disk or Gotek image loaded.

---

## 📁 Repository Structure

```text
fc4msx/
├── gerbers/             # Manufacturing Gerber files & FC4MSX-Gerbers-v1.0.3.zip
├── bom/                 # Interactive BOM (ibom.html) and BOM.md
├── 3d-enclosure/        # 3D printable shell (.STL and .3MF files)
├── docs/                # Assembly guide, pinouts, and hardware notes
│   ├── ASSEMBLY.md      # Step-by-step soldering and pre-power checklist
│   └── PINOUT.md        # 34-pin floppy interface pinout & drive select
├── images/              # PCB 3D renders and preview photos
├── LICENSE              # CC BY-NC-SA 4.0 license details
└── README.md            # Project documentation
```

---

## 📜 Credits & Acknowledgments

- **Talent TDC-600:** Original hardware architecture inspiration.
- **MSX Community:** Thanks to the MSX Resource Center (MSX.org) and retro-computing community for preserving documentation and technical knowledge.

---

## ⚖️ License & Commercial Use Notice

This work is licensed under the **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)** license.

- **Non-Commercial DIY Builds:** You are welcome to view and download these files, order PCBs for personal use, assemble cartridges for yourself or fellow hobbyists (at cost), and share improvements under the same terms with proper attribution.
- **Commercial Restrictions:** **Commercial production, manufacturing, distribution, or sale of PCBs, assembled cartridges, DIY kits, or enclosure prints is strictly prohibited without prior written approval from the author.**
- For commercial licensing inquiries or manufacturing approval, please open an issue or contact the author.
