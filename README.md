# Analog Circuit Design Project

This repository contains the implementation and documentation for five analog circuit designs completed. The circuits include a Ring Oscillator, Voltage Controlled Oscillator (VCO), Wien Bridge Oscillator, Analog Mixer, and Linear Power Supply. Each circuit was designed, simulated, and tested to meet specific objectives, using tools like LT Spice XVII for simulations.

## Project Overview

The project focuses on practical analog circuit design, emphasizing CMOS technology, frequency control, feedback mechanisms, signal mixing, and power regulation. The designs were implemented, under the supervision of Dr. Thayaparan Subramaniam, with contributions from Malanban K., Manimohan T., and Pasqual A.C.

## Circuit Designs

### 1. Ring Oscillator
- **Objective**: Design a ring oscillator using CMOS NOT gates and analyze gate delay and frequency response.
- **Implementation**:
  - Designed a CMOS inverter with pmos4 and nmos4 transistors.
  - Measured gate delay (average 355 ps without parasitics, 365.3 ps with parasitics).
  - Constructed a 7-stage ring oscillator, achieving 25.4 MHz frequency with a 50% duty cycle.
- **Key Observations**:
  - PMOS width set to twice NMOS width to balance rise/fall times.
  - Parasitic capacitances increased gate delay.
  - Transistor length/width variations affected delay and frequency.
- **Challenges**:
  - Precise calibration of transistor parameters.
  - Balancing rise and fall times.

### 2. Voltage Controlled Oscillator (VCO)
- **Objective**: Develop a VCO for communication applications, optimized for low cost, low power, and high stability.
- **Implementation**:
  - Modified ring oscillator with header/footer switches, controlled by voltages \( V_{CP} \) and \( V_{CN} \).
  - Achieved frequencies from 0.956 MHz to 6.464 MHz by varying control voltages.
  - Modified for single control voltage \( V_C \) using current mirroring.
- **Key Observations**:
  - Linear frequency response in the 1.75 V to 2.75 V range.
  - Waveform improved by setting output inverter \( \text{TOX} = 300 \, \text{nm} \).
  - Peak-to-peak voltage slightly below supply due to channel resistances.
- **Challenges**:
  - Achieving linear frequency response.
  - Reducing noise at waveform edges.

### 3. Wien Bridge Oscillator
- **Objective**: Design a Wien Bridge Oscillator for a 32 kHz typical frequency, analyzing feedback and power supply effects.
- **Implementation**:
  - Selected resistor and capacitor values for a frequency range of 29 kHz to 35 kHz, accounting for 10% resistor tolerances.
  - Tested frequency stability under power supply variations.
- **Key Observations**:
  - Sustained oscillations achieved via positive feedback.
  - Frequency range limited by component tolerances and amplifier gain.
- **Challenges**:
  - Precise component selection for target frequency.
  - Managing resistor tolerances.

### 4. Analog Mixer
- **Objective**: Design a diode-based mixer for frequency conversion in RF systems, with filtering to enhance signal quality.
- **Implementation**:
  - Used a 1 MHz sine wave and 10 kHz triangular wave as inputs.
  - Set resistor values (\( R_1 = 100 \, \Omega \), \( R_2 = 100 \, \Omega \), \( R_3 = 1 \, \text{k}\Omega \)).
  - Implemented a bandpass filter to clean the RF signal.
- **Key Observations**:
  - Diodes generated new frequencies via nonlinear operation.
  - Optimized resistor values improved the output spectrum.
- **Challenges**:
  - Calibrating resistors for optimal spectrum.
  - Designing effective bandpass filters.

### 5. Linear Power Supply
- **Objective**: Create a fast-charging linear power supply with adjustable output voltage and effective regulation.
- **Implementation**:
  - Designed for 14 V to 16 V input, 1.5 A current limit, and 6 V to 12 V output range.
  - Used TIP31C, BD139, BC109 transistors, and 1N4732A zener diode (\( V_Z = 4.7 \, \text{V} \)).
  - Selected \( R_1 = 105.26 \, \Omega \), \( R_2 = 1 \, \text{k}\Omega \).
  - Tested line and load regulation.
- **Key Observations**:
  - Minimal output voltage variation under line/load changes.
  - Two zener diodes used in parallel to handle power dissipation.
- **Challenges**:
  - Selecting appropriate zener diodes and transistors.
  - Achieving precise resistor values and avoiding transistor burnout.

## Repository Structure
- **/docs**: Final reports for each circuit design (PDF format).
- **/simulations**: LT Spice XVII simulation files (if available).
- **/README.md**: This file, providing an overview of the project.

## Prerequisites
- **Software**: LT Spice XVII for circuit simulations.
- **Hardware**: Standard electronic components (transistors, diodes, resistors, capacitors) as specified in each design.

## Installation and Usage
1. Clone the repository:
   ```bash
   https://github.com/Manimohan05/Analog_Circuits_Design.git

   ```
2. Open LT Spice XVII and load simulation files from the `/simulations` directory.
3. Refer to the `/docs` directory for detailed circuit designs, parameters, and observations.
4. Replicate circuits using specified components and test under given conditions.

## Challenges and Learnings
- **Component Selection**: Precise selection of components (e.g., zener diodes, resistors) was critical across all designs.
- **Calibration**: Fine-tuning parameters like transistor widths, resistor values, and control voltages required iterative testing.
- **Stability**: Achieving stable oscillations and clean signals posed challenges, addressed through careful design and filtering.
- **Practical Issues**: Transistor burnout and component tolerances highlighted the importance of robust design practices.


## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments
We thank the Department of Electronic & Telecommunication Engineering at the University of Moratuwa for providing the resources and guidance for this project.
