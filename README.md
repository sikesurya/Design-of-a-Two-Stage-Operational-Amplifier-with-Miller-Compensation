# Design of a Two-Stage Operational Amplifier with Miller Compensation

A complete Opamp design project with extensive focus on amplifier specifications, implemented in a TSMC 180nm BSIM3 Level 49 CMOS model environment.

## Overview
This project presents the complete design and simulation procedure for a two-stage CMOS operational amplifier utilizing Miller compensation. The design focuses on meeting specific performance targets and has been rigorously verified through LTSPICE simulations.

## Technology & Tools
* **Technology Node:** TSMC 180nm BSIM3 Level 49 CMOS
* **Simulation Tool:** LTSPICE

## Simulated Performance Results
The OPAMP was simulated using LTspice, achieving the following results which successfully satisfied the target specifications:

| OPAMP PARAMETERS | THEORITICAL VALUES (Required) | ACTUAL VALUES |
| :--- | :--- | :--- |
| **AC Gain(dB)** | 60 dB | 60.43 dB |
| **Phase Margin(deg)** | > 60° | 63.04° |
| **Unity Gain Bandwidth (MHz)** | 30 MHz | 28.065 MHz |
| **Common Mode Gain(dB)** | -11.47 dB | -14.451 dB |
| **CMRR(dB)** | 71.47 dB | 74.451 dB |
| **Slew Rate(V/uS)** | 20 V/uS | 20V/uS |
| **PSRR(dB)** | - 77.327 dB | -77.327 dB |
| **Power Dissipation(No Inputs) (uW)** | < 300 uW | 287.08 uW |

## References
1. Behzad Razavi. *Design of Analog CMOS Integrated Circuits*. McGraw Hill Higher Education; 2001.
2. P. E. Allen, D. R. Holberg. *CMOS Analog Circuit Design*. Oxford University Press; 2002.
3. R. Jacob Baker. *CMOS Circuit Design, Layout, and Simulation*. IEEE Press Series on Microelectronic Systems; 2010.
4. David Johns, Kenneth W. Martin. *Analog Integrated Circuit Design*. Wiley; 1997.
5. Maloberti, Franco. *Analog Design for CMOS VLSI Systems*. Springer; 2001.
