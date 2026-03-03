# Multi-Stage Operational Amplifier Design
**Comprehensive Design and LTspice Simulation of a High-Gain Op-Amp**

## Overview
This project involves the design, analysis, and simulation of a multi-stage CMOS Operational Amplifier. The design was optimized to meet specific engineering constraints, focusing on high open-loop gain, stability, and the ability to drive low-resistance loads.

## Technical Specifications
| Parameter | Target Requirement | Achieved Result |
| :--- | :--- | :--- |
| **Open-Loop Gain** | 80 dB | **82.8 dB** |
| **Gain-Bandwidth Product (GBW)** | 5 MHz | **4.74 MHz** |
| **Phase Margin** | Stable | **-163.6° (at Unity Gain)** |
| **Load Resistance** | 100 Ω | **100 Ω** |
| **Supply Voltage** | ± 3.3 V | **± 3.3 V** |

## System Architecture
The amplifier is divided into four functional sub-circuits, ensuring a modular and robust design:

1. **Bias Branch (Current Mirror):** A cascode current mirror configuration used to provide stable reference currents across all stages with high output impedance.
2. **Differential Amplifier Stage:** The input stage featuring an active load and a cascode current source to maximize CMRR (Common-Mode Rejection Ratio) and provide the initial 40dB gain.
3. **Gain Stage:** A Common-Source amplifier providing an additional 40dB gain. It includes a **25pF Miller Compensation Capacitor** to ensure frequency stability and prevent oscillations.
4. **Output Buffer:** A current-sink biased stage designed for low output impedance, enabling the system to drive a 100Ω load without significant gain degradation.

## Design Highlights & Challenges
* **Stability Analysis:** Used Bode plots to verify the Phase Margin and Gain Margin, ensuring the amplifier remains stable under closed-loop conditions.
* **Iterative Sizing:** Transistor W/L ratios were iteratively optimized to balance DC operating points with AC performance requirements.
* **Load Matching:** The output stage was specifically tuned to handle high current demands for low-resistance loads.

## Tools Used
* **LTspice:** For DC, AC (Frequency Response), and Transient analysis.

## Visual Documentation Guide

**System Block Diagram:**

<img width="675" height="317" alt="Screenshot 2026-03-03 at 14 32 05" src="https://github.com/user-attachments/assets/bdaf09d2-6220-4c86-a504-c4d3de1e6713" />

**Full Circuit Schematic:**

<img width="835" height="394" alt="Screenshot 2026-03-03 at 14 32 14" src="https://github.com/user-attachments/assets/8e5e5319-fa75-452b-ab00-e4c7e7585cf5" />

**Frequency Response (Bode Plot):**

<img width="986" height="533" alt="Screenshot 2026-03-03 at 14 32 25" src="https://github.com/user-attachments/assets/1f4e0c8d-39d6-4900-8ca4-419299504149" />

**Transient Response (Amplified Signal):**

<img width="980" height="530" alt="Screenshot 2026-03-03 at 14 32 45" src="https://github.com/user-attachments/assets/f455e5f1-5aa0-4cfa-a4c4-e61c6db10181" />

---
**Course:** Analog Electronic Circuits | **Institution:** Ruppin Academic Center
