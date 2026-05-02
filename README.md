# CMOS Logic Gates: NAND2, NOR2, and AOI21

## Overview

This repository contains the materials and results for **Laboratory 3: NAND2 and NOR2 Gates**, developed as part of the course *IE03110 – Semiconductor Devices* at the University of Costa Rica.

The objective of this lab is to design, simulate, and analyze **CMOS logic gates**, including:

* NAND2 gate
* NOR2 gate
* Composite gate AOI21

The study focuses on **layout design, DC characteristics, propagation delay, and fan-out effects**.

---

## Contents

The project includes:

* **NAND2 (10/10)**

  * Schematic, layout, and verification
  * Voltage transfer characteristics
  * Delay and fan-out analysis

* **NOR2 (20/5)**

  * Schematic, layout, and verification
  * Voltage transfer characteristics
  * Delay and fan-out analysis

* **AOI21 (Composite Gate)**

  * Schematic, layout, and verification
  * Delay and fan-out analysis 

---

## Tools and Software Used

* **Electric VLSI Design System** (schematic, layout, DRC, NCC)
* **SPICE Simulator** (DC and transient simulations)

> All corresponding files (layouts, schematics, SPICE code, and simulation results) are included in this repository.

---

## 1. NAND2 Gate (10/10)

### Schematic

![NAND2 Schematic](images/NAND_1010/nand2_schematic.png)

### Icon

![NAND2 Icon](images/NAND_1010/nand2_icon.png)

### Layout

![NAND2 Layout](images/NAND_1010/nand2_layout.png)

### DRC & NCC Verification

![NAND2 Verification](images/NAND_1010/nand2_drc.png)

---

### Voltage Transfer Characteristics

#### Vout vs VA

![NAND2 Vout vs VA](images/NAND_1010/nand2_vout_va.png)

#### Vout vs VB

![NAND2 Vout vs VB](images/NAND_1010/nand2_vout_vb.png)

#### Vout vs Vin (A = B)

![NAND2 Vout vs Vin](images/NAND_1010/nand2_vout_vin.png)

### Key Observations

* The NAND2 gate behaves according to its truth table.
* When both inputs are tied together, it behaves as an **inverter**.
* Output transitions follow expected CMOS switching behavior 

---

## 2. NAND2 Delay and Fan-Out Analysis


### Fan-Out FO0

![NAND2 FO0](images/fanout_NAND/nand2_fo0.png)

![NAND2 FO0 Time Results](images/fanout_NAND/nand2_fo0_time_results.png)

### Fan-Out FO4

![NAND2 FO4](images/fanout_NAND/nand2_fo4.png)

![NAND2 FO4 Time Results](images/fanout_NAND/nand2_fo4_time_results.png)


### Fan-Out FO16

![NAND2 FO16](images/fanout_NAND/nand2_fo16.png)

![NAND2 FO16 Time Results](images/fanout_NAND/nand2_fo16_time_results.png)


### Key Observations

* Propagation delay increases with fan-out.
* Higher load results in slower switching times. 

---

## 3. NOR2 Gate (20/5)

### Schematic

![NOR2 Schematic](images/NOR_2005/nor2_schematic.png)

### Icon

![NOR2 Icon](images/NOR_2005/nor2_icon.png)

### Layout

![NOR2 Layout](images/NOR_2005/nor2_layout.png)

### DRC & NCC Verification

![NOR2 Verification](images/NOR_2005/nor2_drc.png)

---

### Voltage Transfer Characteristics

#### Vout vs VA

![NOR2 Vout vs VA](images/NOR_2005/nor2_vout_va.png)

#### Vout vs VB

![NOR2 Vout vs VB](images/NOR_2005/nor2_vout_vb.png)

#### Vout vs Vin (A = B)

![NOR2 Vout vs Vin](images/NOR_2005/nor2_vout_vin.png)

### Key Observations

* The NOR2 gate follows its expected truth table.
* When both inputs are tied together, it also behaves as an **inverter**.
* Output switching characteristics match theoretical expectations 

---

## 4. NOR2 Delay and Fan-Out Analysis

#### Fan-Out FO0

![NOR2 FO0](images/fanout_NOR/nor2_fo0.png)
![NOR2 FO0 Time Results](images/fanout_NOR/nor2_fo0_time_results.png)

#### Fan-Out FO4

![NOR2 FO4](images/fanout_NOR/nor2_fo4.png)
![NOR2 FO4 Time Results](images/fanout_NOR/nor2_fo4_time_results.png)

#### Fan-Out FO16

![NOR2 FO16](images/fanout_NOR/nor2_fo16.png)
![NOR2 FO16 Time Results](images/fanout_NOR/nor2_fo16_time_results.png)

### Fan-Out Key Observations

* Delay increases with fan-out similarly to NAND2.
* Load capacitance significantly affects switching speed. 

---

## 5. Delay Comparison (NAND2 vs NOR2)

### Measurement Results

![Delay Rise Graphic correlation with fan-out](images/delay_graphic_tpdr.png)

![Delay Fall Graphic correlation with fan-out](images/delay_graphic_tpdf.png)

### Key Observations

* Increasing fan-out increases both rise and fall delays.
* NOR2 tends to have faster rising transitions.
* NAND2 tends to have faster falling transitions.
* Average delay:

  * NAND2 ≈ 1.59e-8 s
  * NOR2 ≈ 1.60e-8 s

👉 NAND2 is slightly faster overall 

---

## 6. AOI21 Composite Gate

### Schematic

![AOI21 Schematic](images/AOI21/aoi21_schematic.png)

### Icon

![AOI21 Icon](images/AOI21/aoi21_icon.png)

### Layout

![AOI21 Layout](images/AOI21/aoi21_layout.png)

### DRC & NCC Verification

![AOI21 Verification](images/AOI21/aoi21_drc.png)

---

## 7. AOI21 Delay and Fan-Out FO4 Analysis

### Simulation AOI21 Input A 

![AOI21 Simulation A](images/AOI21/fanout_AOI21/aoi21_delay_a.png)

![AOI21 Simulation Time Results A](images/AOI21/fanout_AOI21/aoi21_fo0_time_results_a.png)

### Simulation AOI21 Input C 

![AOI21 Simulation](images/AOI21/fanout_AOI21/aoi21_delay_c.png)
![AOI21 Simulation Time Results C](images/AOI21/fanout_AOI21/aoi21_fo0_time_results_c.png)


### Key Observations

* Different inputs exhibit different delay behaviors.
* Input A is faster overall based on average delay.
* Input-dependent delay is important in complex gates 

---

## Results Summary

* Successful design and verification of CMOS logic gates.
* Validation of expected logic behavior for NAND2 and NOR2.
* Demonstrated impact of **fan-out on propagation delay**.
* Identified performance differences between gate types.
* Analyzed delay behavior in a composite gate (AOI21).

---

## Author

**Josué María Jiménez Ramírez**
Student – Electrical Engineering
University of Costa Rica 

---
