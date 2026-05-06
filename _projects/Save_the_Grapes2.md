---

layout: project
title: MAE2250 VineGuard Project
description: Grapevine Redirection and Attraction System for Spotted Lanternfly Mitigation
image: /assets/images/SLF-Adult_on_grapes.jpg
technologies:

* Written Report

---

# Grapevine Redirection and Attraction for Pest Elimination (VineGuard)

**Team:** Save the Grapes
**Client(s):** Cornell CALS Extension / E&J Gallo Winery / National Grape

Brief context: This project explores a bio-inspired diversion system designed to attract spotted lanternflies away from grape vines using a combination of chemical attractants, vibration cues, and controlled fluid delivery systems.

---

## Table of Contents

* [Client Pitch (O3)](#client-pitch)
* [Functional Prototype (O5)](#functional-prototype)
* [Client Report](#client-report)

---

## Client Pitch (O3)

### Problem Statement

Spotted lanternflies (SLFs) land on grape vines and feed on sap, contaminating harvests and reducing grape quality. They also promote mold growth, which harms vine health. Studies show up to 22.9 lanternflies per vine, while even 1–2 insects per 1000g sample can lead to rejected shipments. Current pesticide methods are temporary and may damage vines.

This motivates a non-invasive diversion strategy rather than direct removal.

### Impact

SLFs significantly reduce grape yield and quality, threatening vineyard profitability and wine production consistency. Effective mitigation would improve crop reliability, reduce losses, and stabilize market prices.

---

### Concept A: False Grape Vine

**Idea:** Create artificial vines that attract SLFs away from real crops.

* Deployed selectively throughout vineyard
* Contains Tree-of-Heaven-inspired attractant sap
* Includes 60 Hz vibration emitter to enhance attraction
* SLFs preferentially land on fake vines instead of real ones

#### Improvement Over Current Methods

* No pesticide reapplication required every few days
* Non-invasive to real vines
* Designed to integrate into existing vineyard layouts

#### End-of-Semester Prototype

* Single artificial vine structure
* 3D printed + wood frame
* Vibration emitter (60 Hz)
* Fluid reservoir simulating attractant sap

---

### Key Risks

**Risk 1: Space usage in vineyards**
Trap placement may interfere with crop density. We will evaluate performance vs. size tradeoffs.

**Risk 2: Non-target attraction**
Device may attract unintended insects or animals. Field monitoring will be required before scaling.

---

### Client Questions

1. Available spacing for trap deployment within vineyards?
2. Typical vineyard geometry (row spacing, trellis structure, terrain)?
3. Regulatory or environmental constraints for deployed devices?

---

### References

* MSU Extension: Tree of Heaven and SLF interaction
* Penn State Extension: Spotted Lanternfly Management in Vineyards

---

### Figure

<div style="text-align: left;">
  <img src="{{ '/assets/images/figure-2-avg-of-slf-adults-per-vine.png' | relative_url }}" alt="Lantern Fly Density on Grape Vines" style="max-width:100%; height:auto;">
</div>

---

## Functional Prototype (O5)

### Design Documentation

<h3 id="functional-prototype"></h3>

### Design Intent

The prototype demonstrates a fluid-based attraction and dispersion system integrated into an artificial vine structure.

<div style="text-align: center;">
  <img src="{{ '/assets/images/I2.png' | relative_url }}" style="max-width:80%; height:auto;">
</div>

### CAD Assembly

<div style="text-align: center;">
  <img src="{{ '/assets/images/I3.png' | relative_url }}" style="max-width:80%; height:auto;">
</div>

---

### Assembly Process

#### Box Base

* Balsa wood frame
* 3D printed door and frame
* Screws, washers, nuts, hinges
* Hand tools: saw, hole saw

Key dimensions:

* 10 in x 4 in top/long sides
* 8 in x 4 in front/back

Assembly involves constructing a reinforced box frame using corner brackets and attaching a hinged access door for maintenance.

---

#### PVC Pipe & Tubing System

Materials:

* 25 ft 5 mm tubing
* PVC pipe (36 in)
* 3D printed shower head

Flow routing:

* Inner tubing (vinegar): 43 in
* Wrapped tubing (sap): 96 in

System wraps tubing externally around PVC, with micro-slits for controlled leakage.

---

### Design Testing

Two experiments validated fluid delivery:

#### Test 1: Incision Flow

* Average flow rate: ~3 mL/min
* Demonstrated controlled micro-leakage through tubing cuts

#### Test 2: Shower Head Flow

* Flow rate: ~90 mL/min
* Higher output due to larger cross-sectional area

<div style="text-align: center;">
  <img src="{{ '/assets/images/I4.png' | relative_url }}" style="max-width:100%; height:auto;">
</div>

<div style="text-align: center;">
  <img src="{{ '/assets/images/I5.png' | relative_url }}" style="max-width:100%; height:auto;">
</div>

---

### Success Criteria

1. **Sap drainage < 20 mL/hr**
   Current system exceeds target; future work includes flow restriction and pump modulation.

2. **Spray radius > 0.25 m control target**
   Design refinement needed for directional spray containment.

3. **All electronics + reservoirs ≤ 320 in³**
   Requires optimized internal packaging.

---

### Demonstration Criteria

Key visible success metric: controlled spray radius demonstrating effective pest redirection capability.

---

## Client Report

(To be completed or integrated depending on final submission requirements.)

This section will summarize:

* Final system performance
* Design iteration outcomes
* Comparison against success criteria
* Recommendations for scaling to vineyard deployment

---
