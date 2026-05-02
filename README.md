# VLSI Design Laboratory Portfolio

## Overview

This repository contains a collection of laboratory projects developed as part of the course **IE03110 – Semiconductor Devices** at the University of Costa Rica.

The labs progressively explore the fundamentals of **Very-Large-Scale Integration (VLSI)** design, covering:

* Device-level behavior (MOSFETs)
* CMOS logic design
* Combinational circuits
* Sequential circuits and timing analysis

Each laboratory includes **schematic design, layout implementation, SPICE simulation, and performance analysis**, following a complete VLSI design flow.

---

## What is VLSI?

**Very-Large-Scale Integration (VLSI)** refers to the process of integrating thousands to millions of transistors into a single chip.

This field combines:

* **Device physics** (transistor behavior)
* **Circuit design** (logic gates, timing)
* **Layout design** (physical implementation)
* **Verification and simulation** (SPICE, DRC, etc.)

The labs in this repository replicate a simplified version of an **industry VLSI workflow**, moving from transistor-level understanding to complex digital systems.

---

## Repository Structure

Each laboratory is organized in its own branch:

### 📚 Index of Labs

* **Lab 1 – MOSFET Characterization**
  🔗 *[View Lab 1](https://github.com/josveji/VLSI-Semiconductor-Labs/tree/lab1-mosfet-characterization)*
  Study of NMOS and PMOS behavior through Ids–Vds curves and operating regions.

* **Lab 2 – CMOS Inverters**
  🔗 *[View Lab 2](https://github.com/josveji/VLSI-Semiconductor-Labs/tree/lab2-cmos-inverter-analysis)*
  Design and analysis of CMOS inverters, including voltage transfer characteristics, noise margins, delay, and power.

* **Lab 3 – CMOS Logic Gates**
  🔗 *[View Lab 3](https://github.com/josveji/VLSI-Semiconductor-Labs/tree/lab3-cmos-logic-gates-analysis)*
  Implementation of NAND2, NOR2, and AOI21 gates with delay and fan-out analysis.

* **Lab 4 – Pass Gates, MUXes, and Sequential Circuits**
  🔗 *[View Lab 4](https://github.com/josveji/VLSI-Semiconductor-Labs/tree/lab4-pass-gates-mux-sequential)*
  Design of multiplexers, pass gates, latches, and flip-flops, including timing constraints such as setup time.

---

## VLSI Design Flow Covered

Throughout these labs, the following design flow was implemented:

1. **Schematic Design**
   Circuit-level design of transistors and logic gates

2. **Layout Design**
   Physical implementation following design rules

3. **DRC & Verification**
   Ensuring correctness of layout and connectivity

4. **SPICE Simulation**
   Electrical validation (DC and transient analysis)

5. **Performance Evaluation**

   * Delay
   * Power consumption
   * Noise margins
   * Area trade-offs

---

## Key Learnings

* Understanding of **MOSFET operation and modeling**
* CMOS design trade-offs (**speed vs power vs area**)
* Impact of **transistor sizing** on circuit behavior
* Effects of **fan-out and load capacitance**
* Fundamentals of **sequential logic and timing constraints**
* Practical exposure to **EDA tools and simulation workflows**

---

## Tools and Technologies

* **Electric VLSI Design System** – schematic and layout design
* **SPICE Simulator** – circuit simulation and analysis

---

## Author

**Josué María Jiménez Ramírez**
Electrical Engineering Student
University of Costa Rica

---

## Notes

* Each branch contains complete files for its respective lab, including layouts, schematics, and simulations.
* This repository is intended for **educational and portfolio purposes**.

---

## Future Work

* Extension to more complex digital blocks (ALUs, registers, etc.)
* Integration into larger systems (CPU design)
* Exploration of advanced VLSI topics (timing closure, low-power design)

---
