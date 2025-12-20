---
layout: project
title: ENGRD 2210 Portfolio Assignment
description: Class Assignment
image: /assets/images/kohler-engine.jpg
---

**Collaborators:**  
_[Susanna Aufrichtig](mailto:sma283@cornell.edu), [Trevor Boshnack](mailto:tjb287@cornell.edu), [Camille Eckert](mailto:cse49@cornell.edu)_

## Assignment Background

In ENGRD 2210 - Thermodynamics, we were tasked with selecting a real-world instance of a device or system that we had learned about in class, explaining how it works in detail, and discussing how its performance would change under design or operating condition changes.

## System Background

For this assignment, we will be analyzing and comparing the thermal efficiency of the Rehlko Command PRO CH440 Engine. This is the regulation engine mandated by SAE International for the collegiate Baja SAE Competition.

The engine comes stock as a 14HP, single cylinder, four-stroke engine. However, competition rules mandate aftermarket modifications to limit the engine to 10HP.

Throughout this analysis, most data will be sourced from the manufacturer specification sheet for the CH440 engine and the SAE International Competition Rulebook for the Baja SAE competition.

The analysis will consist of three main parts:

1. **Calculating the efficiency of the engine, modeling it as an ideal air standard Otto Cycle**
2. **Calculating differences in ideal air-standard efficiency between the stock 14HP engine and the limited 10HP configuration**
3. **Comparing both of these ideal efficiencies to the efficiency of the engine in real operating conditions**

## Ideal Air Standard Otto Cycle

First, we will model this system as an ideal air-standard Otto cycle.

Below is a comparison between an actual four-stroke engine and the ideal air standard Otto Cycle.

<div style="text-align: center;">
  <img src="{{ '/assets/images/real-four-stroke.jpg' | relative_url }}" alt="Four-stroke engine cycle" style="max-width:100%; height:auto;">
</div>

The real four stroke engine consists of: (1) intake of fuel-air mixture, (2) compression of air, (3) combustion, (4) expansion of air mixture (power stroke), and (5) exhaust of air and combustion products.

<div style="text-align: center;">
  <img src="{{ '/assets/images/otto-cycle.jpg' | relative_url }}" alt="Ideal air-standard Otto cycle" style="max-width:100%; height:auto;">
</div>

Meanwhile, the ideal air standard assumes a closed system where the steps are: (1) adiabatic compression, (2) constant volume heat addition from a thermal reservoir, (3) adiabatic expansion, and (4) constant volume heat removal to a thermal reservoir.

The efficiency of this ideal system is given by:

$$
\eta = 1 - \left(\frac{1}{r}\right)^{k-1}
$$

where \(r\) is the compression ratio (given by the manufacturer as \(r = 8.3\)) and \(k\) is the specific heat ratio (typically \(k = 1.4\) when modeling air as an ideal gas).

Thus we find that:

$$
\eta = 1 - \left(\frac{1}{8.3}\right)^{1.4 - 1} = 0.5711 = 57.11\%.
$$

This is the thermal efficiency for the stock, 14HP engine, and it is within typical values for an ideal air-standard Otto cycle.

## Engine Comparison

### Work and Heat Input Variation

For the Baja SAE competition, the 14 HP engine has an air limiting gasket, making it operate at 10 HP. Since thermal efficiency only depends on the compression ratio, the efficiency between the two engine variations should be the same. We can use physically recorded data to find the difference in the work output and heat input per cycle between the engines.

We start by calculating the cycle work and heat input for a 14HP cycle. Per the CH440 datasheet, the maximum torque output of 22.7 ft-lbs occurs at 2800 rpm.

To calculate power output, we use:

$$
P = \tau \, \omega = \tau \frac{2 \pi \cdot \text{RPM}}{60 \,\text{s}}
$$

Now, to calculate the work, we use the fact that the work of a cycle is power divided by cycles per second. For a four-stroke engine, there is one cycle every 2 revolutions:

$$
W_{\text{cyc}}
= \frac{P}{\text{cycles/sec}}
= \frac{\tau \frac{2 \pi \cdot \text{RPM}}{60 \,\text{s}}}{\frac{\text{RPM}}{2\cdot 60 \,\text{s}}}
= 4\pi\tau
= 4\pi \cdot 30.78\,\text{Nm}
= 386.79\,\text{J}
$$

With the previously calculated efficiency and this newly calculated work per cycle, we can back out the heat input:

$$
Q_{\text{in}} = \frac{W_{\text{cyc}}}{\eta}
= \frac{386.79\,\text{J}}{0.5711}
= 677.28\,\text{J}
$$

Now that we know the heat inputted into the engine, we can calculate new performance metrics for the restricted 10HP engine using measured values for torque and RPM.

These values are obtained thanks to Trevor's work for Cornell Baja Racing last year. Trevor created a dynamometer setup which measured the power band RPM and maximum torque using a hall effect sensor, a load cell, and a water brake.

<div style="text-align: center;">
  <img src="{{ '/assets/images/dyno-setup.png' | relative_url }}" alt="Dynamometer setup" style="max-width:100%; height:auto;">
</div>

The maximum torque was determined to be around 18 ft-lb, and powerband was determined to be at 3000 rpm.

With this information, we repeat the previous calculations to find the work output and heat input of the 10HP cycle. From the previously derived equation for cycle work:

$$
W_{\text{cyc}} = 4\pi\tau
= 4\pi \cdot 24.405\,\text{Nm}
= 306.62\,\text{J}
$$

And using the definition of thermal efficiency once more:

$$
Q_{\text{in}} = \frac{W_{\text{cyc}}}{\eta}
= \frac{306.62\,\text{J}}{0.5711}
= 536.89\,\text{J}
$$

We can see that the work per cycle decreased from 386.79 J to 306.62 J. The heat input per cycle decreased from 677.28 J to 536.89 J. This will result in lower fuel intake, but also a lower maximum torque output.

### Air Intake Limitation

To make this design decision, Rehlko engineers needed to determine how much to limit the air intake to get the torque dropoff of 22.7 ft-lb to 18 ft-lb. The change in the mass of air being consumed can be determined with information we already have.

The mean effective pressure is the average pressure throughout the stroke defined by work of the cycle divided by the displacement:

$$
\text{MEP} = \frac{W_{\text{cyc}}}{V_{\text{d}}}
$$

From the ideal gas law (\(PV=mRT\)), the mass of the air in the cylinder is proportional to the pressure (assuming temperature is approximately constant for this scaling argument). Therefore, the mass of air is proportional to mean effective pressure:

$$
W_{\text{cyc}} \propto \text{MEP} \propto P \propto m_{\text{air}}
$$

We can simplify the work of the cycle to maximum torque since they are proportional:

$$
\tau \propto \text{MEP} \propto m_{\text{air}}
$$

This means the ratios of torque and mass of air should be equivalent:

$$
\frac{\tau_{10}}{\tau_{14}} = \frac{m_{\text{air},10}}{m_{\text{air},14}} = 0.793
$$

We can conclude that the intake should be limited such that only 79.3% of the original air mass can enter the cylinder.

## Real Efficiency

Having analyzed the theoretical efficiency of the CH440 engine modified for use in Baja SAE, we now ask: how does it compare to its real performance in competition?

Thermal efficiency of a power cycle in general is expressed as:

$$
\eta = \frac{W_{\text{cyc}}}{Q_{\text{in}}}
$$

That is, the work produced by a cycle divided by the heat added during the cycle.

To calculate the heat input, we analyze the fuel used for the engine and its lower heating value (LHV). For unleaded gasoline, the typical LHV is 12.2 kWh/kg or 43.92 MJ/kg. Baja SAE rules state all competition vehicles must use Pyrotect Part Number SFC100 as a fuel tank. The dimensions of the fuel tank are shown in the drawing (8.00 in ⌀ x 7.94 in). When full, the volume of fuel inside the tank is:

$$
V = h r^2 = (7.94)(4)^2 = 399.1 \,\text{in}^3 = 0.00654 \,\text{m}^3.
$$

<div style="display: flex; justify-content: space-between; align-items: center;">
  <img src="{{ '/assets/images/baja-fuel-tank.png' | relative_url }}" alt="Fuel tank photo" style="width:48%;">
  <img src="{{ '/assets/images/baja-fuel-tank-drawing.jpg' | relative_url }}" alt="Fuel tank drawing" style="width:48%;">
</div>

The typical density for unleaded gasoline is about 0.71 to 0.77 g/mL (710 to 770 kg/m\(^3\)). To be conservative in our calculation of efficiency, we choose the highest density. Thus, the mass of gas when the gas tank is full is:

$$
m = \rho V = (770)\,(0.00654) = 5.0358 \,\text{kg}.
$$

To calculate the total heat energy that can be obtained from this amount of fuel:

$$
Q = m \cdot \text{LHV} = (5.0358)\,(43.92) = 221.17 \,\text{MJ}.
$$

Now the trickier part: figuring out how much work we get out of one full tank.

To do this, we will analyze Cornell's vehicle’s motion and fuel consumption during the 4-hour Baja SAE Endurance race. Looking at lap times, track length, and fuel consumption during the last Endurance Race, we find that the vehicle started the race with a full fuel tank and stopped to refuel after about 2.25 hours. At this time, Cornell had completed 41 laps. Given that one lap measured about 1.2 miles, the approximate distance traveled by the car on one fuel tank was about 49.275 miles, or 79,300.4256 meters.

To find work, we use:

$$
W = F \, dl \approx F\,l
$$

To find the average force exerted on the car to move it forward, we perform a static calculation. Taking the coefficient of friction between the wheel and a dirt track to be approximately:

$$
\mu = 0.4
$$

The free body diagram for one of the wheels looks as below:

<div style="text-align: center;">
  <img src="{{ '/assets/images/fbd-baja-wheel.png' | relative_url }}" alt="Free body diagram of Baja wheel" style="max-width:100%; height:auto;">
</div>

Multiplying the result of the friction force by four wheels, we find that the total forward force necessary to move the car forward is 889.952 N.

Going back to the work calculation, the work produced by the engine using up one fuel tank is approximately:

$$
W = (889.952)\,(79{,}300.4256) = 70.57 \,\text{MJ}.
$$

We can finally return to the efficiency calculation to find that the real-life efficiency of the engine is approximately:

$$
\eta_{\text{real}} = \frac{70.57}{221.17} = 0.319 = 31.9\%.
$$

As expected, the actual efficiency is much lower than the ideal-air standard efficiency. This is not only due to the real cycle not being ideal air (i.e., not an ideal gas but rather a fuel-air mixture, not isentropic, expansion as a result of combustion rather than heat transfer, etc.) but also due to other broader simplifying assumptions such as assuming only forward motion, assuming constant torque as average torque (when in reality front and rear wheels produce different amounts of torque and torque varies between the transmission’s low and high-end ratios), and assuming perfect torque transmission between the wheels and ground (ignoring wheel slip and losses of energy to friction, air resistance, etc.).

<div style="text-align: center;">
  <img src="{{ '/assets/images/tg21.jpg' | relative_url }}" alt="Cornell Baja vehicle" style="max-width:100%; height:auto;">
</div>
