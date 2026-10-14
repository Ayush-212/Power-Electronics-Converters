# MATLAB / Simulink Power Electronics Converters & Power Delivery Simulations

This repository contains MATLAB scripts, Simulink (`.slx`) models, and simulation results for power electronics converter architecture.

---

## 🛠️ Included Converter Models

### 1. DC-DC Buck Converter (Power Delivery Optimization)
* **Objective:** Step-down DC voltage regulation with closed-loop Pulse-Width Modulation (PWM) control.
* **Key Metrics:** Passive component sizing ($L, C$), ripple constrained to $<3\%$, transient response evaluation under load step changes.

### 2. AC-DC Controlled Semi & Full Converters
* **Objective:** Phase-controlled thyristor rectifiers for high-voltage DC bus generation.
* **Key Metrics:** Firing angle ($\alpha$) variation, Total Harmonic Distortion (THD) analysis, input power factor evaluation.


---

## 📁 Repository Structure
* `/models`: Simulink `.slx` files for Buck, Rectifiers, and Inverter circuits.
* `/scripts`: MATLAB `.m` initialization files for component parameter calculation and FFT harmonic analysis.
* `/waveforms`: Output voltage, current, and THD scope plots.

---

## 💻 Software Requirements
* MATLAB R2025a
* Simulink & Simscape Electrical & Specialized Power Systems Library
