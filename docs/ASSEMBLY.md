# FC4MSX Assembly & Testing Guide

## Assembly Steps

1. **Inspection:** Inspect the bare PCB under good light or magnification. Ensure traces around the 50-pin edge connector are clean with no bridging.
2. **Low-Profile Components First:**
   - Solder passive resistors and diodes.
   - Solder ceramic capacitors (0.1µF decoupling).
3. **Sockets & Connectors:**
   - Solder IC sockets (recommended for DIP ICs to prevent thermal stress and facilitate troubleshooting).
   - Solder the 34-pin boxed shrouded connector.
   - Solder any jumpers or pin headers.
4. **Electrolytic Capacitors & Crystal:**
   - Observe polarity on electrolytic capacitors!
   - Solder the crystal/oscillator.
5. **Clean the Board:**
   - Clean flux residue using isopropyl alcohol (IPA) 99% and a soft brush.
   - Ensure the gold fingers of the cartridge edge connector are completely free of flux or grease.

---

## Pre-Power Checks

1. **Multimeter Continuity & Resistance Check:**
   - Before inserting any ICs into sockets, measure resistance between **VCC (+5V)** and **GND** on the MSX connector pins.
   - Ensure there is NO short circuit (resistance should not be near 0 Ω).
2. **Power Test:**
   - You can measure voltage in-slot or bench power with +5V to verify power rails reach the VCC pins on all IC sockets.

---

## Programming the Disk ROM

1. Obtain or compile a TDC-600 compatible MSX-DOS Disk ROM.
2. Flash the ROM binary to your 27C256 / 28C256 (or compatible EEPROM) using an EPROM programmer (e.g. TL866II / T48).
3. Insert the ROM and logic ICs carefully into their respective sockets, ensuring proper pin 1 orientation.

---

## Testing with MSX

1. Turn off the MSX computer.
2. Insert the FC4MSX cartridge into Cartridge Slot 1 or 2.
3. Connect a tested floppy drive or Gotek (with USB formatted disk containing MSX-DOS).
4. Power on the MSX.
5. You should see the MSX boot logo followed by the floppy drive seek and the MSX-DOS prompt or disk load.
