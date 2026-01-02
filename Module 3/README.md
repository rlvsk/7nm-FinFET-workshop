# Module 3  
**Designing Bandgap References Using 7nm FinFETs**

---

##  Module Goal
This module demonstrates the design of a **temperature-stable voltage reference** using 7nm FinFET models. Since this repo contains no external theory files, the essential concepts are documented directly here.

---

##  Background Concepts

### 1. What is a Bandgap Reference?
A Bandgap Reference (BGR) circuit generates a **constant DC voltage (Vref)** that remains stable even if:
- Temperature varies
- Supply voltage fluctuates
- Device parameters shift at nanoscale nodes  

This makes it a critical block in analog/mixed-signal chips for biasing ADCs, PLLs, power management circuits, and RF systems.

---

### 2. PTAT vs CTAT – The Stability Principle
BGR combines two opposite temperature behaviors:

| Term | Meaning | Temperature Behavior |
|---|---|---|
| **CTAT** | Complement-To-Absolute-Temperature | Voltage ↓ when Temp ↑ |
| **PTAT** | Proportional-To-Absolute-Temperature | Voltage ↑ when Temp ↑ |

When summed in the right ratio, these slopes cancel each other, producing a **flat Vref vs Temperature response**.

---

### 3. Why FinFETs at 7nm Help BGR?
At 7nm, planar BJTs are not available in standard PDKs, so we implement CTAT/PTAT using:
- **Diode-connected NFETs or parasitic BJT effects**
- **Current mirrors built using multi-fin 7nm FETs**

FinFET advantages:
- Low leakage → better bias stability
- Strong gate control → reliable Vt behavior across temperature
- Compact layout → suitable for scaled analog blocks

---

### 4. How Vref is Validated?
Using simulation plots:
- **.dc sweep** → ensures correct bias generation
- **Transient (.tran)** → confirms startup and settling
- **Temperature sweep** → checks Vref flatness
- **Supply current plots** → used to compute power

