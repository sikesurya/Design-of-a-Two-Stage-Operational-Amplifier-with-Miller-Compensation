# Design of a Two-Stage Operational Amplifier with Miller Compensation

A complete Opamp design project with extensive focus on amplifier specifications, implemented in 0.5 µm CMOS technology.

## Overview
This project presents the complete design and simulation procedure for a two-stage CMOS operational amplifier utilizing Miller compensation. The design focuses on meeting specific performance targets and has been rigorously verified through LTSPICE simulations.

## Technology & Tools
* **Technology Node:** 0.5 µm CMOS
* **Simulation Tool:** LTSPICE

## Simulated Performance Results
The OPAMP was simulated using LTspice, achieving the following results which successfully satisfied the target specifications:

| Parameter | Simulated Value |
| :--- | :--- |
| **DC Gain** | 63.5 dB |
| **Phase Margin** | 61.8° |
| **Unity Gain Bandwidth** | 21 MHz |
| **Slew Rate** | 24 V/µs |
| **Power Dissipation** | 1.88 mW |
| **CMRR** | 85.2 dB |
| **ICMR (+)** | 2.45 V |
| **ICMR (-)** | -0.5 V |
| **Output Swing (+)** | 2.3 V |
| **Output Swing (-)** | -2.2 V |

## References
1. Behzad Razavi. *Design of Analog CMOS Integrated Circuits*. McGraw Hill Higher Education; 2001.
2. P. E. Allen, D. R. Holberg. *CMOS Analog Circuit Design*. Oxford University Press; 2002.
3. R. Jacob Baker. *CMOS Circuit Design, Layout, and Simulation*. IEEE Press Series on Microelectronic Systems; 2010.
4. David Johns, Kenneth W. Martin. *Analog Integrated Circuit Design*. Wiley; 1997.
5. Maloberti, Franco. *Analog Design for CMOS VLSI Systems*. Springer; 2001.
