# Analog Circuit Design 

## Overview
This repository contains simulation files, reports, and designs for analog circuits developed as part of the EN3013 - Analog Circuit Design module at the Department of Electronic & Telecommunication Engineering, University of Moratuwa. The projects focus on practical implementations of essential analog circuits:

1. **Analog Mixer Design**
2. **Linear Power Supply Design**
3. **Voltage Controlled Oscillator (VCO) Design**

The repository includes detailed documentation, design methodologies, and simulation results for each project.

---

## Projects

### 1. Analog Mixer Design
**Objective:**
- Understand analog mixers using diodes as key components.
- Explore frequency conversion via nonlinear transfer functions.
- Analyze diode-based mixers and implement filtering techniques for improved performance.

**Features:**
- Circuit design to mix a 1 MHz carrier sine wave and a 10 kHz triangular wave.
- Observations of frequency spectra at the output.
- Implementation of bandpass filtering for signal quality enhancement.

**Challenges:**
- Optimizing circuit parameters for ideal RF spectrum output.
- Filtering out unwanted components from the signal.

---

### 2. Linear Power Supply Design
**Objective:**
- Design a fast-charging, adjustable power supply for modern devices.
- Ensure high load and line regulation with minimal DC ripple and noise.

**Key Parameters:**
- Input Voltage: 16 V
- Output Voltage Range: 9 ± 3 V
- Current Limitation: 1.5 A

**Methodology:**
- Selection of components such as TIP31C, BD139, and BC109.
- Calculations for Zener diodes, resistors, and current limiting.
- Analysis of load and line regulation under varying conditions.

**Challenges:**
- Difficulty sourcing appropriate components.
- Achieving the specified output range and resolving initial circuit inconsistencies.

---

### 3. Voltage Controlled Oscillator (VCO) Design
**Objective:**
- Design a VCO for communication systems, focusing on cost-effectiveness, low power consumption, and high stability.
- Analyze its performance in applications like PLL circuits and frequency synthesizers.

**Procedure:**
- Utilize a ring oscillator with header and footer switches.
- Experiment with control voltages to optimize output frequency.
- Modify the circuit to include a common control voltage.

**Observations:**
- Output frequency varies linearly with control voltage in the range of 1.75 V to 2.75 V.
- Adjustments to transistor parameters improved the output waveform.

---

## Repository Structure
```
├── Analog Mixer Design
│   ├── Design Files
│   ├── Simulation Results
│   └── Report.pdf
├── Linear Power Supply Design
│   ├── Design Files
│   ├── Simulation Results
│   └── Report.pdf
├── Voltage Controlled Oscillator Design
│   ├── Design Files
│   ├── Simulation Results
│   └── Report.pdf
└── README.md
```

---

## How to Use
1. Clone the repository: `git clone <repository_url>`
2. Navigate to the project folder of interest.
3. Refer to the design files and reports for implementation details and results.

---

## Contributors
- **Malamban K. (200373X)**
- **Manimohan T. (200377M)**
- **Pasqual A.C. (200445V)**

**Supervisors:** Dr. Thayaparan Subramaniam

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## Acknowledgments
This work was completed as part of the EN3013 - Analog Circuit Design module at the University of Moratuwa. Special thanks to our supervisors and instructors for their guidance.


