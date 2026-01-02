# 7nm FinFET Workshop – Module 2  
**Device & Inverter Characterization, SPICE Modelling, and Performance Analysis at 7nm**

---

## 9. NFET Characteristics Using 7nm PDKs
This section covers NMOS (NFET) device behavior using 7nm Process Design Kits. Key parameters explored:

- Output and transfer characteristics  
- Impact of fin dimensions on current drive  
- Leakage trends at scaled nodes  
- Gate control efficiency in multi-gate structures  

The goal is to understand how a 7nm NFET responds to different bias conditions and physical constraints.

---

## 10. Inverter Characteristics Using 7nm FinFETs
Focuses on CMOS inverter behavior built using 7nm FinFET transistors.

Topics include:

- Voltage transfer curve (VTC) shape and interpretation  
- Symmetry between pull-up and pull-down networks  
- Effect of fin count on switching behavior  
- Power-delay tradeoffs in scaled logic  

This stage ensures understanding of inverter response before SPICE-level modelling.

---

## 11. Inverter SPICE Deck & Characteristics Modelling
Covers how to write and model an inverter using a SPICE simulation file (deck).

Core learnings:

- Defining MOS models from 7nm PDK libraries  
- Applying DC, transient, and AC analyses  
- Exporting key waveform data  
- Structuring simulation outputs for characterization  

This bridges transistor models with circuit-level simulation behavior.

---

## 12. Analysis of W/L Ratio, Vt, Power, Prop Delay, Gain & Noise Margin
Performance parameters studied:

| Parameter | Purpose |
|---|---|
| W/L Ratio | Balances drive strength of PMOS/NMOS |
| Threshold Voltage (Vt) | Determines switching point |
| Power Consumption | Measures static + dynamic power |
| Propagation Delay | Evaluates speed of transition |
| Gain | Slope of VTC (amplification ability) |
| Noise Margin | Circuit robustness against noise |

The objective is to model how sizing and threshold shifts impact energy, speed, and stability at 7nm.

---

## 13. Transconductance, Frequency & Characterization Table Assignment
Introduces AC behavior and frequency response of the inverter.

Includes:

- Transconductance (**gm**) extraction  
- 3dB cutoff frequency estimation  
- Unity-gain frequency understanding  
- Tabulating results into a comparison table  

You will generate a final characterized device + circuit parameter table as part of this assignment.

---

## 14. Lab Tips – Switching Threshold, Drain Current & Power Calculation
Practical methods to compute:

- Switching threshold voltage (from VTC)  
- Drain current at different gate bias points  
- Power using `P = V × I` principle  
- Identifying operating regions (linear/sat) from curves  

Focus is on correct measurement from simulation rather than theoretical equations.

---

## 15. Lab Tips – Prop Delay, gm & Frequency Calculation
Hands-on guidance to extract:

- Propagation delay from transient waveform (50% crossing method)  
- Transconductance from transfer slope  
- Frequency limits from AC response  
- Best practices for clean measurement (small step size, stable biasing, minimizing noise)  

---

## 16. Assignment
### Deliverables expected:
- NFET characteristic plots  
- Inverter VTC, transient, and AC response  
- Extracted Vt, delay, power, gm, and frequency values  
- Final characterization table  
- Observations on scaling tradeoffs  

---

## Module 2 Folder Structure (recommended)
