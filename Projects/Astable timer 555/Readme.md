
# 555 Timer Astable Oscillator PCB

## Overview

This repository contains the schematic and PCB design files for a classic **555 Timer Astable Oscillator**. The circuit is designed to generate a continuous square wave, which drives an LED to blink at a stable, calculated frequency. The board is compact and designed using EasyEDA.

### 3D PCB Render

> **Note:** Replace the image below with your actual 3D render.
> 

## Circuit Details

In this astable configuration, the NE555 timer continuously triggers itself, producing a steady stream of output pulses without requiring external intervention.
With the selected component values, the LED blinks at a comfortable, highly visible rate of approximately **1.38 Hz**.

### Schematic Diagram

### Mathematical Calculation

The frequency of the output square wave is determined by the timing resistors ($R_A$ and $R_B$) and the timing capacitor ($C$). The standard formula is:

$$f = \frac{1.44}{(R_A + 2R_B)C}$$

Given the components used in this schematic:

* $R_A = 10\text{k}\Omega$
* $R_B = 47\text{k}\Omega$
* $C = 10\mu\text{F}$

The resulting frequency is:

$$f = \frac{1.44}{(10000 + 94000) \times 10 \times 10^{-6}} \approx 1.38 \text{ Hz}$$

## Bill of Materials (BOM)

* **U1:** NE555P Timer IC
* **R_A:** 10kΩ Resistor
* **R_B:** 47kΩ Resistor
* **R1:** 220Ω Resistor (LED Current Limiting)
* **C:** 10µF Capacitor (Timing)
* **U2:** 10nF / 0.01µF Capacitor (Control Voltage decoupling)
* **LED1:** 0603 SMD Red LED
* **H1:** 2-Pin Connector (2.54mm pitch) for VCC and GND input

## Repository Structure

* `Hardware/` : Contains the EasyEDA source files (Schematic and PCB layout in JSON format).
* `Production/` : Contains the generated Gerber files for PCB manufacturing and the BOM (CSV).
* `Images/` : Contains screenshots of the theoretical schematic and the 3D render of the final PCB.

