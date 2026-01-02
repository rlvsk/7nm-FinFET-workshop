# Module 2  
**Lab-to-Simulatio: 7nm FinFET Devices and Innovations**

---

##  Overview
This module focuses on **device-level and circuit-level characterization** of 7nm NFETs and CMOS inverters using industry-style simulation flows. All measurements and results are extracted from SPICE and visualized using plots.


---

##  Core Concepts

### 1. NFET (NMOS) Characteristics at 7nm
At 7nm, NFETs use a multi-gate fin structure that offers:
- Strong gate control → reduced leakage
- Higher drive current using multiple fins
- Better short channel effect suppression

#### Two main curves studied:
- **Output Characteristics (Id vs Vds):** shows current behavior as drain voltage increases
- **Transfer Characteristics (Id vs Vgs):** shows how current increases with gate voltage and helps extract **threshold voltage (Vt)**

---

### 2. 7nm CMOS Inverter Characteristics
A CMOS inverter is built using:
- 7nm **PFET (PMOS)** as pull-up
- 7nm **NFET (NMOS)** as pull-down

#### Key behavior insights:
- When input is LOW → PFET ON, NFET OFF → Vout ≈ VDD
- When input is HIGH → NFET ON, PFET OFF → Vout ≈ GND
- The switching point depends on:
  - W/L ratio
  - Threshold voltage
  - Number of fins
  - Device strength balance

---

### 3. Performance Parameters Extracted from Plots
| Parameter | How it's measured |
|---|---|
| **Threshold Voltage (Vt)** | From Id–Vgs curve (transfer plot) |
| **Gain** | From slope of VTC curve |
| **Noise Margin** | From inverter VTC plot using VIH/VIL points |
| **Propagation Delay** | From transient plot using 50% input–output crossing |
| **Power (Static + Dynamic)** | Using supply current from plots (`P = VDD × Iavg`) |
| **gm (Transconductance)** | From derivative/slope of transfer curve |
| **Cutoff Frequency (f3dB)** | From AC response plot of inverter |

These parameters help evaluate **speed, stability, and energy efficiency trade-offs at 7nm**.



