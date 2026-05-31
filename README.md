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

## AC Analysis
![AC Gain Plot](path/to/ac_gain_plot.png) <!-- Please upload and replace with the actual path to your plot image -->

AC analysis of an OTA is used to determine its frequency response, including gain and bandwidth. By applying a small-signal AC input, parameters like gain, phase margin, and unity-gain bandwidth can be evaluated. It helps in assessing the stability and performance of the amplifier in the frequency domain. **The AC Gain = 60.43 dB, which is near the required gain 60 dB and Phase Margin = 63.04°, greater than 60°.**

## DC Analysis
![DC Analysis Plot](path/to/dc_analysis_plot.png) <!-- Please upload and replace with the actual path to your plot image -->

DC Analysis of an OTA is used to study its steady-state behavior by sweeping input voltages. It helps determine parameters like operating point, output swing, and input common-mode range (ICMR). This analysis ensures that the transistors operate in the correct region for proper amplifier functioning. **ICMR ≈ 0.7 V to 1.6 V.**

## Slew Rate
![Slew Rate Plot](path/to/slew_rate_plot.png) <!-- Please upload and replace with the actual path to your plot image -->

Slew rate: Which is measured in volts per microsecond, is the fastest rate at which an op amp's output voltage can fluctuate. The slew rate is calculated by introducing a significant signal step, such as one volt, to the op amp's input.
**ΔV = 1.06 - 0.94 = 0.12V.**
**Δt = 12 - 6 = 6ns.**
**SR = 0.12 / 6 = 0.02V/ns = 20V/us.**
Thus we get the exact slew rate that we want.

## Common Mode Gain
![Common Mode Gain Plot](path/to/common_mode_gain_plot.png) <!-- Please upload and replace with the actual path to your plot image -->

COMMON MODE GAIN: Common-mode gain of an OTA represents the amplification of signals that are identical at both inputs. Ideally, it should be very low to reject noise and interference present on both inputs. It is used to evaluate the common-mode rejection capability of the amplifier. **Here the Common Mode Gain we are getting is around -14.451dB, which is near to what we theoretically want.**

## Power Supply Rejection Ratio (PSRR)
![PSRR Plot](path/to/psrr_plot.png) <!-- Please upload and replace with the actual path to your plot image -->

PSRR: Power Supply Rejection Ratio (PSRR) measures the ability of an OTA to suppress variations in the power supply voltage. It indicates how much supply noise affects the output.
A high PSRR ensures better stability and accurate signal amplification in the presence of supply fluctuations. **Getting PSRR around -77.327 dB.**

## Common-Mode Rejection Ratio (CMRR)
![CMRR Plot](path/to/cmrr_plot.png) <!-- Please upload and replace with the actual path to your plot image -->

CMRR (Common-Mode Rejection Ratio) is a measure of how well a differential amplifier rejects signals that are common to both inputs (common-mode signals). It is defined as the ratio of differential gain to common-mode gain. A higher CMRR means better ability to amplify only the desired differential signal while ignoring noise or interference.

`CMRR(dB) = 20 log (Ad / Acm) = Ad(dB) - Acm(dB)`

**Therefore CMRR = AC Gain - Common Mode Gain = 60.43 dB - (-14.451 dB) = 74.451 dB.**

## References
1. Behzad Razavi. *Design of Analog CMOS Integrated Circuits*. McGraw Hill Higher Education; 2001.
2. P. E. Allen, D. R. Holberg. *CMOS Analog Circuit Design*. Oxford University Press; 2002.
3. R. Jacob Baker. *CMOS Circuit Design, Layout, and Simulation*. IEEE Press Series on Microelectronic Systems; 2010.
4. David Johns, Kenneth W. Martin. *Analog Integrated Circuit Design*. Wiley; 1997.
5. Maloberti, Franco. *Analog Design for CMOS VLSI Systems*. Springer; 2001.
