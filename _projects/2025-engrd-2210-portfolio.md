---
layout: project
title: ENGRD 2210 Portfolio Assignment
description: Class Assignment
image: /assets/images/kohler-engine.jpg
technologies:
  - Rehlko CH440 datasheet
  - SAE Baja Rules
  - Cornell Baja dyno data
---

**Collaborators:**  
_[Susanna Aufrichtig](mailto:sma283@cornell.edu), [Trevor Boshnack](mailto:tjb287@cornell.edu), [Camille Eckert](mailto:cse49@cornell.edu)_

## Assignment Background

In ENGRD 2210 - Thermodynamics, we were tasked with selecting a real-world instance of a device or system that we had learned about in class, explaining how it works in detail, and discussing how its performance would change under design or operating condition changes.

## System Background

For this assignment, we analyze and compare the thermal efficiency of the Rehlko Command PRO CH440 engine, the regulation engine mandated by SAE International for the collegiate Baja SAE competition.

The engine comes stock as a 14HP, single-cylinder, four-stroke engine. However, competition rules mandate aftermarket modifications that limit the engine to 10HP.

Throughout this analysis, most data is sourced from the manufacturer specification sheet for the CH440 engine and the SAE Baja SAE competition rulebook.

The analysis consists of three parts:

1. **Calculating the efficiency of the engine, modeling it as an ideal air-standard Otto cycle**
2. **Calculating differences in ideal air-standard efficiency between the stock 14HP engine and the limited 10HP configuration**
3. **Comparing both of these ideal efficiencies to the efficiency of the engine in real operating conditions**

## Ideal Air-Standard Otto Cycle

First, we model this system as an ideal air-standard Otto cycle.

Below is a comparison between an actual four-stroke engine and the ideal air-standard Otto cycle.

<div style="text-align: center;">
  <img src="{{ '/assets/images/real-four-stroke.jpg' | relative_url }}" alt="Four-stroke engine cycle" style="max-width:100%; height:auto;">
</div>

The real four-stroke engine consists of: (1) intake of fuel-air mixture, (2) compression, (3) combustion, (4) expansion (power stroke), and (5) exhaust.

<div style="text-align: center;">
  <img src="{{ '/assets/images/otto-cycle.jpg' | relative_url }}" alt="Ideal air-standard Otto cycle" style="max-width:100%; height:auto;">
</div>

Meanwhile, the ideal air-standard Otto cycle assumes a closed system where the steps are: (1) adiabatic compression, (2) constant-volume heat addition from a thermal reservoir, (3) adiabatic expansion, and (4) constant-volume heat removal to a thermal reservoir.

The thermal efficiency of the ideal air-standard Otto cycle is:

$$
\eta = 1 - \left(\frac{1}{r}\right)^{k-1}
$$

where r = 8.3 is the compression ratio specified by the manufacturer, and k = 1.4 is the specific heat ratio for air modeled as an ideal gas.

Substituting values:

$$
\eta = 1 - \left(\frac{1}{8.3}\right)^{1.4-1}
= 0.5711
= 57.11\%
$$

This is the thermal efficiency for the stock 14HP engine, and it is within typical values for an ideal air-standard Otto cycle.

## Engine Comparison

### Work and Heat Input Variation

For the Baja SAE competition, the 14HP engine has an air limiting gasket, making it operate at 10HP. Since ideal Otto cycle efficiency depends only on compression ratio, the ideal air-standard efficiency for the two configurations should be the same. We can use measured data to estimate differences in work output and heat input per cycle.

We start by calculating the cycle work and heat input for the 14HP configuration. Per the CH440 datasheet, the maximum torque output of 22.7 ft-lb occurs at 2800 rpm.

To calculate power output:

$$
P = \tau \omega = \tau\frac{2\pi \cdot \mathrm{RPM}}{60\,\mathrm{s}}
$$

For a four-stroke engine, there is one cycle every two revolutions, so:

$$
\mathrm{cycles/sec} = \frac{\mathrm{RPM}}{2\cdot 60}
$$

Thus, work per cycle is:

$$
W_{\mathrm{cyc}}
= \frac{P}{\mathrm{cycles/sec}}
= \frac{\tau \frac{2\pi \cdot \mathrm{RPM}}{60\,\mathrm{s}}}{\frac{\mathrm{RPM}}{2\cdot 60\,\mathrm{s}}}
= 4\pi\tau
$$

Converting torque to SI units:

$$
W_{\mathrm{cyc}} = 4\pi \cdot 30.78\,\mathrm{N\cdot m}
= 386.79\,\mathrm{J}
$$

Using the efficiency to back out heat input:

$$
Q_{\mathrm{in}} = \frac{W_{\mathrm{cyc}}}{\eta}
= \frac{386.79}{0.5711}
= 677.28\,\mathrm{J}
$$

Now we calculate performance metrics for the restricted 10HP engine using measured values for torque and RPM.

These values are obtained from Trevor’s work for Cornell Baja Racing last year. Trevor built a dynamometer setup measuring power band RPM and maximum torque using a hall effect sensor, a load cell, and a water brake.

<div style="text-align: center;">
  <img src="{{ '/assets/images/dyno-setup.png' | relative_url }}" alt="Dynamometer setup" style="max-width:100%; height:auto;">
</div>

The maximum torque was determined to be around 18 ft-lb, and the power band was determined to be at 3000 rpm.

Using the same expression:

$$
W_{\mathrm{cyc}} = 4\pi\tau
= 4\pi \cdot 24.405\,\mathrm{N\cdot m}
= 306.62\,\mathrm{J}
$$

And heat input:

$$
Q_{\mathrm{in}} = \frac{W_{\mathrm{cyc}}}{\eta}
= \frac{306.62}{0.5711}
= 536.89\,\mathrm{J}
$$

Work per cycle decreased from 386.79 J to 306.62 J, and heat input per cycle decreased from 677.28 J to 536.89 J. This implies lower fuel intake at peak conditions, but also a lower maximum torque output.

### Air Intake Limitation

To reduce torque from 22.7 ft-lb to 18 ft-lb, engineers must limit air intake. The change in air mass consumption can be estimated using mean effective pressure.

Mean effective pressure is defined as:

$$
\mathrm{MEP} = \frac{W_{\mathrm{cyc}}}{V_d}
$$

From the ideal gas law, the air mass in the cylinder scales with pressure as a rough proportionality argument. Therefore:

$$
W_{\mathrm{cyc}} \propto \mathrm{MEP} \propto P \propto m_{\mathrm{air}}
$$

Since work per cycle is proportional to torque for this comparison:

$$
\tau \propto \mathrm{MEP} \propto m_{\mathrm{air}}
$$

So the ratio of torque should approximate the ratio of air mass:

$$
\frac{\tau_{10}}{\tau_{14}}
= \frac{m_{\mathrm{air},10}}{m_{\mathrm{air},14}}
= 0.793
$$

Therefore, the intake should be limited such that only 79.3% of the original air mass can enter the cylinder.

## Real Efficiency

Having analyzed the theoretical efficiency of the CH440 engine modified for use in Baja SAE, we now ask: how does it compare to real performance in competition?

Thermal efficiency is:

$$
\eta = \frac{W_{\mathrm{cyc}}}{Q_{\mathrm{in}}}
$$

To estimate heat input over a tank, we use the fuel lower heating value (LHV). For unleaded gasoline, a typical LHV is 12.2 kWh/kg (43.92 MJ/kg). Baja SAE rules require Pyrotect Part Number SFC100 as the fuel tank. From the tank drawing (8.00 in ⌀ × 7.94 in), approximating it as a cylinder:

$$
V = h r^2 = (7.94)(4)^2 = 399.1\,\mathrm{in^3} = 0.00654\,\mathrm{m^3}
$$

<div style="display: flex; justify-content: space-between; align-items: center;">
  <img src="{{ '/assets/images/baja-fuel-tank.png' | relative_url }}" alt="Fuel tank photo" style="width:48%;">
  <img src="{{ '/assets/images/baja-fuel-tank-drawing.jpg' | relative_url }}" alt="Fuel tank drawing" style="width:48%;">
</div>

The density of unleaded gasoline is approximately 0.71 to 0.77 g/mL (710 to 770 kg/m³). To be conservative, we use the highest value:

$$
m = \rho V = (770)(0.00654) = 5.0358\,\mathrm{kg}
$$

Total heat energy available from one full tank is:

$$
Q = m \cdot \mathrm{LHV} = (5.0358)(43.92) = 221.17\,\mathrm{MJ}
$$

Next, we estimate how much work the vehicle produces on one full tank.

From endurance race lap logs, Cornell’s vehicle started with a full tank and refueled after about 2.25 hours. By then, Cornell completed 41 laps. With lap length about 1.2 miles, the distance traveled per tank is:

- 49.275 miles
- 79,300.4256 meters

To estimate work:

$$
W = \int F\,dl \approx F\,l
$$

To approximate forward force, we use a friction-limited estimate with coefficient of friction:

$$
\mu = 0.4
$$

The free body diagram for one wheel is shown below:

<div style="text-align: center;">
  <img src="{{ '/assets/images/fbd-baja-wheel.png' | relative_url }}" alt="Free body diagram of Baja wheel" style="max-width:100%; height:auto;">
</div>

Multiplying the friction force by four wheels gives a total forward force of 889.952 N.

Thus:

$$
W = (889.952)(79{,}300.4256) = 70.57\,\mathrm{MJ}
$$

Finally, the estimated real-life efficiency is:

$$
\eta_{\mathrm{real}} = \frac{70.57}{221.17} = 0.319 = 31.9\%
$$

As expected, the actual efficiency is much lower than the ideal air-standard efficiency. This is due to real-cycle effects (non-isentropic compression/expansion, irreversibilities, heat transfer, and combustion losses) and broader simplifying assumptions (forward-motion-only assumption, constant average force/torque assumption, and ignoring wheel slip and losses to drivetrain friction, rolling resistance, and aerodynamic drag).

<div style="text-align: center;">
  <img src="{{ '/assets/images/tg21.jpg' | relative_url }}" alt="Cornell Baja vehicle" style="max-width:100%; height:auto;">
</div>
