# AMS1117 5.0V Linear Voltage Regulator Module

## Overview
This repository contains the schematic and PCB layout for a robust and compact 5V linear voltage regulator module based on the **AMS1117-5.0**. Designed with proper thermal management and manufacturer-recommended decoupling, this board is ideal for powering microcontrollers, IoT devices, and other embedded systems.

### 3D PCB Render

![3D View of the PCB](https://github.com/shereifDev/PCB-Design/blob/main/Projects/Voltage%20Regulator/Images/3D.png)


## Key Features
- **Stable 5V Output:** Reliable step-down conversion from a 6.5V-12V input source.
- **Optimized Thermal Design:** Features a dedicated copper pour (GND plane) under the AMS1117 tab to maximize heat dissipation and prevent thermal shutdown.
- **Power Indicator:** Includes an ultra-low current SMD LED (0603) paired with a 2.2kΩ resistor for safe and efficient power status indication.
- **Clean Power Delivery:** Integrates input (10uF) and output (22uF) decoupling capacitors to ensure loop stability and rapid transient response.
- **EDA Tool:** Designed and routed using EasyEDA.

## Bill of Materials (BOM)

| Reference | Component | Value / Part Number | Package | Description |
| :--- | :--- | :--- | :--- | :--- |
| **U1** | LDO Voltage Regulator | AMS1117-5.0 | SOT-223 | Fixed 5.0V Output LDO |
| **C1** | Input Capacitor | 10uF | SMD | Filters input noise |
| **C2** | Output Capacitor | 22uF | SMD | Ensures stability & response |
| **R1** | Resistor | 2.2kΩ | SMD 0603 | Current limiting for LED |
| **LED1** | LED | Red/Green | SMD 0603 | Power indicator |
| **H1, H2** | Pin Headers | 1x2 Male Header | 2.54mm Pitch | Input and Output terminals |

## Design Guidelines Followed
1. **Trace Widths:** Power traces (`VIN`, `VOUT`) are routed with a width of `0.6mm - 0.8mm` to safely handle up to 1A of current without significant voltage drops.
2. **Ground Plane:** A continuous GND polygon pour is applied across the board, providing a low-impedance return path and enhancing the module's thermal relief capabilities.
3. **Component Placement:** Capacitors are placed as close to the IC pins as possible to minimize parasitic inductance.

