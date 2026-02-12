# Heart-Shaped 555 Timer PCB  
PCB Milling Project – Creative Embedded Systems

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

## Hardware Requirements
- Carvey CNC machine (or comparable PCB-capable CNC)
- 1/64" end mill (traces)
- 1/32" end mill (outline)
- Soldering iron and solder
- CR2032 3V coin battery
- CR2032 battery holder

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


## Reproduction Instructions
### CNC Milling
- `simple_drill.svg`: drill holes
- `simple_front.svg`: isolation traces
- `simple_outline.svg`: heart outline

### Soldering
Using the diagram below or the kicad files, solder the hardware components accordingly.
<img width="707" height="722" alt="Screenshot 2026-02-12 at 12 54 35 AM" src="https://github.com/user-attachments/assets/366ab773-fb47-4fb9-ae76-92f63527fa1e" />
