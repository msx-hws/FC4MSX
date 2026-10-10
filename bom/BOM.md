# Bill of Materials (BOM) - FC4MSX

This document lists the components required to assemble the FC4MSX floppy controller cartridge.

| Designator | Description | Package / Footprint | Quantity | Notes |
| :--- | :--- | :--- | :--- | :--- |
| **U1** | Floppy Disk Controller (WD2793 / equivalent) | DIP-40 | 1 | Match TDC-600 controller architecture |
| **U2** | Disk ROM (27C256 / 27C128 / 28C256) | DIP-28 | 1 | Programmed with TDC-600 compatible MSX-DOS Disk ROM |
| **U3..Ux** | Glue Logic ICs (74LS / 74HCT series) | DIP-14 / DIP-16 / DIP-20 | As per schematic | Standard TTL / HCT logic |
| **Y1** | Crystal / Oscillator | HC-49S or DIP-4 / DIP-8 | 1 | Typically 4 MHz / 8 MHz / 16 MHz per design |
| **J1** | 34-Pin Shrouded IDC Header (FDD connector) | 2x17 pin 2.54mm pitch | 1 | Keyed box header recommended |
| **C_dec** | Decoupling Capacitors (100nF / 0.1µF) | Ceramic 2.54mm pitch | ~6-10 | One per IC power pin |
| **C_bulk**| Bulk Filter Capacitor (10µF - 47µF, 16V+) | Radial Electrolytic | 1-2 | Near power input rails |
| **R_pull**| Pull-up Resistors / Resistor Network | SIP-9 / SIP-10 or 1/4W Through-hole | Various | ~1kΩ - 4.7kΩ for bus pull-ups & floppy signals |
| **LED1**  | Activity / Power LED (Optional) | 3mm Through-hole | 1 | Green / Amber / Red |
| **R_led** | Current-limiting Resistor for LED | 0.25W Through-hole (330Ω - 1kΩ) | 1 | |

---

### Sockets & Hardware
- **DIP Sockets:** High-quality machined (round-pin) or dual-wipe DIP sockets are strongly recommended for the FDC IC (DIP-40) and ROM (DIP-28) to allow easy swapping/testing.
- **Enclosure Fasteners:** M2 / M2.5 self-tapping or countersunk machine screws (check `3d-enclosure/README.md` for exact length).
