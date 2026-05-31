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
<img width="789" height="378" alt="image" src="https://github.com/user-attachments/assets/1ff87d3f-e7e4-43ef-ad7c-0c5e4e849a46" />


AC analysis of an OTA is used to determine its frequency response, including gain and bandwidth. By applying a small-signal AC input, parameters like gain, phase margin, and unity-gain bandwidth can be evaluated. It helps in assessing the stability and performance of the amplifier in the frequency domain. **The AC Gain = 60.43 dB, which is near the required gain 60 dB and Phase Margin = 63.04°, greater than 60°.**

## DC Analysis
<img width="748" height="332" alt="image" src="https://github.com/user-attachments/assets/d2c7671d-be48-4cc7-851d-47ba94733dd1" />


DC Analysis of an OTA is used to study its steady-state behavior by sweeping input voltages. It helps determine parameters like operating point, output swing, and input common-mode range (ICMR). This analysis ensures that the transistors operate in the correct region for proper amplifier functioning. **ICMR ≈ 0.7 V to 1.6 V.**

## Slew Rate
<img width="788" height="376" alt="image" src="https://github.com/user-attachments/assets/099640ae-df9d-4582-85cc-7dd6aaa129e0" />

Slew rate: Which is measured in volts per microsecond, is the fastest rate at which an op amp's output voltage can fluctuate. The slew rate is calculated by introducing a significant signal step, such as one volt, to the op amp's input.
**ΔV = 1.06 - 0.94 = 0.12V.**
**Δt = 12 - 6 = 6ns.**
**SR = 0.12 / 6 = 0.02V/ns = 20V/us.**
Thus we get the exact slew rate that we want.

## Common Mode Gain
<img width="788" height="375" alt="image" src="https://github.com/user-attachments/assets/6ccc7662-5c50-49cf-846d-e7c7ba20a1e3" />


COMMON MODE GAIN: Common-mode gain of an OTA represents the amplification of signals that are identical at both inputs. Ideally, it should be very low to reject noise and interference present on both inputs. It is used to evaluate the common-mode rejection capability of the amplifier. **Here the Common Mode Gain we are getting is around -14.451dB, which is near to what we theoretically want.**

## Power Supply Rejection Ratio (PSRR)
<img width="788" height="374" alt="image" src="https://github.com/user-attachments/assets/7feb54b2-a26c-4473-9e0f-11a4ad7af871" />


PSRR: Power Supply Rejection Ratio (PSRR) measures the ability of an OTA to suppress variations in the power supply voltage. It indicates how much supply noise affects the output.
A high PSRR ensures better stability and accurate signal amplification in the presence of supply fluctuations. **Getting PSRR around -77.327 dB.**

## INPUT COMMON MODE RANGE:
<img width="787" height="377" alt="image" src="https://github.com/user-attachments/assets/8b3eb4b6-446c-433d-853f-1b7d74900aab" />

ICMR: Input common mode range(ICMR) is calculated by providing negative feedback to
the opamp. In this scenario opamp acts as a unity gain buffer. ICMR ≈ 0.7 V to 1.6 V.


## References
1. Behzad Razavi. *Design of Analog CMOS Integrated Circuits*. McGraw Hill Higher Education; 2001.
2. P. E. Allen, D. R. Holberg. *CMOS Analog Circuit Design*. Oxford University Press; 2002.
3. R. Jacob Baker. *CMOS Circuit Design, Layout, and Simulation*. IEEE Press Series on Microelectronic Systems; 2010.
4. David Johns, Kenneth W. Martin. *Analog Integrated Circuit Design*. Wiley; 1997.
5. Maloberti, Franco. *Analog Design for CMOS VLSI Systems*. Springer; 2001.




