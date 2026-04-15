# hybrid-energy-storage-system
Designed a dual source energy circuit to eliminate battery transient 
# Hybrid Energy Storage System (HESS) for High-Efficiency Lighting

**What it does:** Combines a LiFePO4 battery and a 20F supercapacitor 
with MPPT and active power sharing to supply a lighting load with 
minimal battery stress and maximum efficiency.

**The technical challenge:** Dynamically allocating load between two 
storage elements with different characteristics (energy-dense battery 
vs power-dense supercapacitor) using only an MCU and MOSFET switches.

**Tech used:** LiFePO4 · Supercapacitor (20F) · MPPT · Embedded C · 
MOSFET switching · Thermal protection circuits

## How it works
- MPPT algorithm tracks maximum power point, achieving ~98% conversion 
  efficiency (experimentally measured)
- SOC-based power management logic decides in real time how load is 
  split between battery and supercapacitor
- Synchronous rectification via MCU-controlled MOSFETs with 10ms 
  dead-time eliminates diode conduction losses
- Dual-stage thermal cutoff circuits protect both storage elements 
  from overtemperature faults
- Active power sharing reduced peak battery discharge current by ~40%, 
  extending battery cycle life

## Results
- ~40% reduction in peak battery discharge current

