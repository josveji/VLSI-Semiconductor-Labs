# CMOS Inverter Design and Analysis

## Overview

This repository contains the materials and results for **Laboratory 2: Inverters**, developed as part of the course *IE03110 – Semiconductor Devices* at the University of Costa Rica .

The objective of this lab is to design, simulate, and analyze **CMOS inverters** with different sizing ratios. The study includes layout design, DC and transient simulations, and evaluation of key performance metrics such as **voltage transfer characteristics, noise margins, delay, and power consumption**.

---

## Contents

The project includes the design and analysis of three CMOS inverters:

* **20/10 inverter**
* **10/10 inverter**
* **15/5 inverter**

For each inverter:

* Schematic design
* Symbol (icon) creation
* Layout design
* DRC and NCC verification

Additionally:

* Voltage Transfer Characteristics (Vout vs Vin)
* Noise margin analysis
* Propagation delay analysis
* Power consumption analysis 

---

## Tools and Software Used

* **Electric VLSI Design System** (schematic, layout, and verification)
* **SPICE Simulator** (DC and transient simulations)
* **LaTeX** (report documentation)

> All corresponding files (schematics, layouts, SPICE code, and simulation results) are attached in this repository.

---

## 1. CMOS Inverter Designs

### 1.1 Inverter 20/10

#### Schematic

![Inverter 20/10 Schematic](images/inverter_20_10_schematic.png)

#### Icon

![Inverter 20/10 Icon](images/inverter_20_10_icon.png)

#### Layout

![Inverter 20/10 Layout](images/inverter_20_10_layout.png)

#### DRC & NCC Verification

![Inverter 20/10 DRC](images/inverter_20_10_drc.png)

---

### 1.2 Inverter 10/10

#### Schematic

![Inverter 10/10 Schematic](images/inverter_10_10_schematic.png)

#### Icon

![Inverter 10/10 Icon](images/inverter_10_10_icon.png)

#### Layout

![Inverter 10/10 Layout](images/inverter_10_10_layout.png)

#### DRC & NCC Verification

![Inverter 10/10 DRC](images/inverter_10_10_drc.png)

---

### 1.3 Inverter 15/5

#### Schematic

![Inverter 15/5 Schematic](images/inverter_15_5_schematic.png)

#### Icon

![Inverter 15/5 Icon](images/inverter_15_5_icon.png)

#### Layout

![Inverter 15/5 Layout](images/inverter_15_5_layout.png)

#### DRC & NCC Verification

![Inverter 15/5 DRC](images/inverter_15_5_drc.png)

---

## 2. Voltage Transfer Characteristic (VTC)

### SPICE Setup

![SPICE Code VTC](images/spice_vtc.png)

### Simulation Cell

![Simulation Cell](images/simulation_cell_vtc.png)

### Vout vs Vin Curves

![VTC Curves](images/vtc_curves.png)

*Different curves correspond to different inverter sizing ratios.*

---

## 3. Noise Margin Analysis

![Noise Margin](images/noise_margin.png)

Noise margins were calculated using:

* ( NMH = V_{OH} - V_{IH} )
* ( NML = V_{IL} - V_{OL} )

### Key Observations

* The **10/10 inverter (1:1 ratio)** provides a more balanced switching point.
* Increasing the PMOS/NMOS ratio shifts the switching threshold.
* Larger asymmetry leads to different high/low noise margins. 

---

## 4. Sizing Analysis

* The ratio between PMOS and NMOS widths directly affects the switching voltage.
* Inverters closer to a **1:1 ratio switch earlier**.
* Higher ratios (e.g., 3:1) shift inversion to higher input voltages.

---

## 5. Propagation Delay

### SPICE Setup

![SPICE Delay](images/spice_delay.png)

### Simulation

![Delay Simulation](images/delay_simulation.png)

### Vin and Vout vs Time

![Delay Curves](images/delay_curves.png)

### Key Observations

* Rise and fall times are approximately equal for properly sized inverters.
* A **2:1 ratio** helps balance charging and discharging times. 

---

## 6. Power Analysis

### Current vs Time

![Current Curve](images/current_vs_time.png)

### Output Voltage vs Time

![Vout Curve](images/vout_vs_time.png)

### Power Consumption

![Power Curve](images/power_vs_time.png)

### Key Observations

* Power consumption peaks during switching events.
* NMOS transistors switch faster but consume more power.
* PMOS transistors are slower but more power-efficient. 

---

## Results Summary

* Successful design and verification of three CMOS inverters.
* Clear relationship between transistor sizing and switching behavior.
* Validation of theoretical expectations:

  * Trade-off between speed and power
  * Impact of sizing on noise margins
  * Balanced delay achieved with proper sizing

---

## Author

**Josué María Jiménez Ramírez**
Student – Electrical Engineering
University of Costa Rica 

---
