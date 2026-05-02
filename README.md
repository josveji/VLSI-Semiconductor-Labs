# Pass Gates, Multiplexers, and Sequential Elements

## Overview

This repository contains the materials and results for **Laboratory 4: Pass Gates, Multiplexers, and Sequential Elements**, developed as part of the course *IE03110 – Semiconductor Devices* at the University of Costa Rica .

The objective of this lab is to design, simulate, and analyze **combinational and sequential CMOS circuits**, including:

* Pass gates
* Multiplexers (Mux 2:1)
* D Latch
* D Flip-Flop

The study focuses on **layout design, functional verification, delay analysis, and timing constraints**.

---

## Contents

The project includes:

* **Pass Gate**

  * Schematic, layout, and simulation

* **Mux 2:1 (Pass Gate Implementation)**

  * Design and verification

* **Mux 2:1 (NAND2 Implementation)**

  * Design and comparison

* **Mux Comparison**

  * Area and delay analysis

* **D Latch**

  * Design and transient behavior

* **D Flip-Flop**

  * Design and timing analysis (setup time) 

---

## Tools and Software Used

* **Electric VLSI Design System** (schematic, layout, DRC)
* **SPICE Simulator** (transient simulations and delay analysis)

> All corresponding files (schematics, layouts, SPICE code, and simulation results) are included in this repository.

---

## 1. Pass Gate

### Schematic

![Pass Gate Schematic](images/Pass_Gate/pass_gate_schematic.png)

### Icon

![Pass Gate Icon](images/Pass_Gate/pass_gate_icon.png)

### Layout

![Pass Gate Layout](images/Pass_Gate/pass_gate_layout.png)

### DRC Verification

![Pass Gate DRC](images/Pass_Gate/pass_gate_drc.png)

---

### Simulation

#### Simulation Cell & SPICE Setup

![Pass Gate Simulation Cell](images/Pass_Gate/pass_gate_simulation.png)

#### Output Behavior

![Pass Gate Waveform](images/Pass_Gate/pass_gate_waveform.png)

### Key Observations

* The pass gate correctly transmits the input signal when enabled.
* Complementary control signals ensure proper switching behavior. 

---

## 2. Mux 2:1 (Pass Gate Implementation)

### Schematic

![Mux Pass Gate Schematic](images/Mux_2_1_pass_gate/mux_pass_schematic.png)

### Icon

![Mux Pass Gate Icon](images/Mux_2_1_pass_gate/mux_pass_icon.png)

### Layout

![Mux Pass Gate Layout](images/Mux_2_1_pass_gate/mux_pass_layout.png)

### DRC Verification

![Mux Pass Gate DRC](images/Mux_2_1_pass_gate/mux_pass_drc.png)

---

## 3. Mux 2:1 (NAND2 Implementation)

### Schematic

![Mux NAND Schematic](images/Mux_2_1_NAND2/mux_nand_schematic.png)

### Icon

![Mux NAND Icon](images/Mux_2_1_NAND2/mux_nand_icon.png)

### Layout

![Mux NAND Layout](images/Mux_2_1_NAND2/mux_nand_layout.png)

### DRC Verification

![Mux NAND DRC](images/Mux_2_1_NAND2/mux_nand_drc.png)

---

## 4. Mux Comparison

### Area Comparison

| 2:1 MUX Type       | Height (λ) | Length (λ) | Area (λ²) |
|--------------------|------------|------------|-----------|
| Pass Gate          | 80         | 123        | 9840      |
| NAND2              | 80         | 273        | 21840     |

*Table 1: MUX area comparison.*

👉 NAND implementation is ~2.2× larger 

---

### Delay Analysis

#### NAND-Based MUX

![Mux NAND Delay Time Results](images/MuxDelay/mux_nand_delay_graph.png)

![Mux NAND Delay Time Results](images/MuxDelay/mux_nand_delay_time.png)

#### Pass-Gate MUX

![Mux NAND Delay Time Results](images/MuxDelay/mux_nand_delay_graph.png)

![Mux Pass Delay Time Results](images/MuxDelay/mux_pass_delay_time.png)

#### Comparison

| MUX Type         | Rise Time (ns)        | Fall Time (ns)         |
|------------------|-----------------------|------------------------|
| Pass Transistor  | 5.69 × 10⁻¹¹          | 6.03 × 10⁻¹¹           |
| NAND2            | 2.63 × 10⁻¹⁰          | 1.97 × 10⁻¹⁰           |

*Table 2: Delay data for 2:1 MUX types.*

### Key Observations

* Pass-gate MUX has significantly lower delay.
* NAND-based MUX introduces more delay due to higher transistor count.
* Trade-off:

  * **Pass gate → faster and smaller**
  * **NAND → slower but more controlled timing** 

---

## 5. D Latch

### Schematic

![D Latch Schematic](images/Latch_D/d_latch_schematic.png)

### Icon

![D Latch Icon](images/Latch_D/d_latch_icon.png)

### Layout

![D Latch Layout](images/Latch_D/d_latch_layout.png)

### DRC Verification

![D Latch DRC](images/Latch_D/d_latch_drc.png)

---

### Simulation

![D Latch Simulation](images/Latch_D/d_latch_waveform.png)

### Key Observations

* The latch is **transparent when clock = 1**.
* When clock = 0, it **holds the previous value**.
* Correct storage behavior was verified 

---

## 6. D Flip-Flop

### Schematic

![D Flip-Flop Schematic](images/FF_D/dff_schematic.png)

### Icon

![D Flip-Flop Icon](images/FF_D/dff_icon.png)

### Layout

![D Flip-Flop Layout](images/FF_D/dff_layout_full.png)

### DRC Verification

![D Flip-Flop DRC](images/FF_D/dff_drc.png)

---

### Simulation

![D Flip-Flop Waveform](images/FF_D/dff_waveform.png)

### Key Observations

* Data is captured on the **rising edge of the clock**.
* Output remains stable between clock edges.
* Behavior matches expected D flip-flop operation 

---

## 7. Setup Time Analysis

![Setup Time](images/FF_D/setup_time.png)

![Setup Time Zoom In](images/FF_D/setup_time_zoom_in.png)

### Results

* Minimum setup time ≈ **0.3 ns**

### Key Observations

* Data must arrive before the clock edge to be properly stored.
* If the setup time is violated, the output fails to capture the input. 

---

## Results Summary

* Successful design and verification of pass gates and multiplexers.
* Demonstrated trade-offs between **area and delay** in MUX implementations.
* Correct operation of sequential elements (Latch and Flip-Flop).
* Identification of critical timing parameter (**setup time**).

---

## Author

**Josué María Jiménez Ramírez**
Student – Electrical Engineering
University of Costa Rica 

---
