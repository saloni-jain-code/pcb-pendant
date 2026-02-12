# PCB Pendant
Creative Embedded Systems

## Overview

This project is a custom heart-shaped printed circuit board (PCB) that uses a 555 timer chip mode to blink a red LED. The board was designed in KiCad, converted to CNC-compatible SVG files, and milled on a CNC machine.
![Heart PCB Blinking](pcb_pendant.gif)

This repository contains the design files and manufacturing exports necessary to reproduce the PCB (assuming access to required hardware and tools).

## Repository Structure
- `/kicad` contains the original schematic and PCB layout files.
- `/manufacturing` contains SVG files used for CNC milling:
  - Isolation traces
  - Drill holes
  - Board outline

## Materials and Components
- Single-sided copper board for PCB
- CR2032 3V coin battery
- CR2032 battery holder
- 555 timer chip
- Red LED (5mm)
- Resistor R1: 4.7k ohms
- Resistor R2: 68k ohms
- Resistor R3: 470 ohms
- Capacitor C1: 10 nF
- Capacitor C2: 4.7 uF
<img width="796" height="499" alt="Screenshot 2026-02-12 at 12 49 17 AM" src="https://github.com/user-attachments/assets/a0f2eca0-2204-4382-ac27-af25f8a4d036" />

## CNC Milling Instructions

The provided SVG files are ready for milling in Easel.  
Files included:
- `simple_front.svg` (isolation traces)
- `simple_drill.svg` (drill holes)
- `simple_outline.svg` (heart board outline)
### 1. Easel Setup
Set material dimensions:
- **Material Type:** PCB
- **Width:** 152 mm
- **Length:** 106 mm
- **Thickness:** 1.6 mm
Secure the copper board to the machine bed.
## Step 1: Mill Isolation Traces
1. Select bit:
   - **V Bit – Custom 30° PCB**
   - Change to this bit in the CNC machine too
2. Import:
   - `simple_front.svg`
3. In **Cut Settings**:
   - Depth: **0.08 mm**
   - If traces are not fully isolated, increase to **0.13 mm**
4. Positioning:
   - Move the design outside of the clamp/red zone
   - Place it toward the **bottom right** of the material
5. Import `simple_outline.svg`
   - Align it with your PCB
   - Record the X and Y position values
   - Delete the heart outline before carving
6. Click **Carve**
## Step 2: Drill Holes
1. Import:
   - `simple_drill.svg`
2. Manually align drill holes to match the milled traces.
3. Delete the isolation trace geometry (only drill holes should remain).
4. Change bit to:
   - **End Mills → Upcut 1/32 in Fishtail Spiral (0.8 mm)**
5. Right-click drill geometry → **Convert to Drill Holes**
6. Cut settings:
   - Depth: **1.6 mm**
   - **Add Depth: +0.2 mm**
7. Click **Carve**
## Step 3: Cut Board Outline
1. Remove drill hole geometry.
2. Import:
   - `simple_outline.svg`
3. Set X and Y positions using the values recorded earlier.
4. Change bit to:
   - **1/8 in Double Flute Straight End Mill**
5. Set:
   - Tabs: **2 tabs**
   - Tab length: **2 mm**
6. Click **Carve**
After carving, carefully remove the board and cut tabs manually if needed.

### Soldering
Using the diagram below or the kicad files, solder the hardware components listed above accordingly.
<img width="707" height="722" alt="Screenshot 2026-02-12 at 12 54 35 AM" src="https://github.com/user-attachments/assets/366ab773-fb47-4fb9-ae76-92f63527fa1e" />
