layout: project
title: ENGRD 2210 Portfolio Assignment
description: Class Assignment
image: /assets/images/kohler-engine.jpg
---

## **Collaborators:** ##
_[Susanna Aufrichtig](mailto:sma283@cornell.edu), [Trevor Boshnack](mailto:tjb287@cornell.edu), [Camille Eckert](mailto:cse49@cornell.edu)_

## Assignment Background

In ENGRD 2210 - Thermodynamics, we were tasked with selecting a real-world instance of a device or system that we had learned about in class, explaining how it works in detail, and discussing how its perforamnce would change under design or operating condition changes.

## System Background

For this assignment, we will be analyzing and comparing the thermal efficiency of the Rehlko Command PRO CH440 Engine. This is the regulation engine mandated by SAE International for the collegiate Baja SAE Competition.

The engine comes stock as a 14HP, single cylinder, four-stroke engine. However, competition rules mandate aftermarket modifications to limit the engine to 10HP.

Throughout this analysis, most data will be sourced from the manufacturer specification sheet for the CH440 engine and the SAE International Competition Rulebook for the Baja SAE competition.

The analysis will consist of three main parts:

**1. Calculating the efficiency of the engine, modeling it as a ideal air standard Otto Cycle**

**2. Calculate differences in ideal air-standard efficiency between the stock 14HP engine and the limitted 10HP configuration.**

**3. Compare both of these ideal efficiencies to the efficiency of the engine in real operating conditions**

## Ideal Air Standard Otto Cycle

First, we will model this system as an ideal air-standard Otto cycle.

Below is a comparison between an actual four-stroke engine and the ideal air standard Otto Cycle.

<div style="text-align: center;">
  <img src="{{ '/assets/images/real-four-stroke.jpg' | relative_url }}" alt="Centered Image" style="max-width:100%; height:auto;">
</div>

The real four stroke engine consists of 1. intake of fuel-air mixture 2. compression of air 3. combustion 4. expansion of air mixture (power stroke) 5. exhaust of air and combustion products.

<div style="text-align: center;">
  <img src="{{ '/assets/images/otto-cycle.jpg' | relative_url }}" alt="Centered Image" style="max-width:100%; height:auto;">
</div>

Meanwhile, the ideal air standard assumes a closed system where the steps are 1. adiabatic compression 2. constant pressure heat addition from a thermal reservoir 3. adiabatic expansion 4. constant pressure heat removal to a thermal reservoir.

The efficiency of this ideal system is given by the equation:

{% raw %}
$$
\eta = 1 - \left(\frac{1}{r}\right)^{k-1}
$$
{% endraw %}

where r is the compression ratio (given by the manufacturer as r = 8.3) and k is the specific heat ratio, typically k = 1.4 when modeling air as an ideal gas.

Thus we find that:

{% raw %}
$$
\eta = 1 - \left(\frac{1}{8.3}\right)^{1.4 - 1} = 0.5711 = 57.11\%.
$$
{% endraw %}

This is the thermal efficiency for the stock, 14HP engine, and it is within typical values for an ideal air-standard Otto cycle.

## Engine Comparison

#### Work and Heat Input Variation

For the Baja SAE competition, the 14 HP engine has an air limiting gasket, making it operate at 10 HP. Since thermal efficiency only depends on the compression ratio, the efficiency between the two engine variations should be the same. We can use physically recorded data to find the difference in the work output and heat input per cycle between the engines.

We start by calculating the cycle work and heat input for a 14HP cycle. Per the CH440 datasheet, the maximum torque output of 22.7 ft-lbs occurs at 2800 rpm.

To calculate power output, we use

{% raw %}
$$
P = \tau \, \omega = \tau \frac{2 \pi \cdot RPM}{\text{60 sec}}
$$
{% endraw %}

Now, to calculate the work, we use the fact that the work of a cycle is power per cycles per second:

{% raw%}
$$
W_\text{cyc} = \frac{P}{\text{cycles/sec}} = \frac{\tau \frac{2 \pi \cdot RPM}{\text{60 sec}}}{\frac{RPM}{\text{2 cyles*60sec}}} = 4 \pi \tau = 4 \pi \cdot \text{30.78 Nm} = \text{386.79 J}
$$
{% endraw %}

With the previously calculated efficiency and this newly calculated work per cycle, we can back out the heat inputted:

{% raw %}
$$
Q_\text{in} = \frac{W_\text{cyc}}{\eta} = \frac{\text{386.79 J}}{0.5711} = \text{677.28 J}
$$
{% endraw %}

Now that we know the heat inputted into the engine, we can calculate new performance metrics for the restricted 10HP engine using measured values for torque and RPM.

These values are obtained thanks to Trevor's work for Cornell Baja Racing last year. Trevor created a dynamometer setup which measured the power band RPM and maximum torque using a hall effect sensor, a load cell, and a water break.

<div style="text-align: center;">
  <img src="{{ '/assets/images/dyno-setup.png' | relative_url }}" alt="Centered Image" style="max-width:100%; height:auto;">
</div>

The maximum torque was determined to be around 18 ft-lb, and powerband was determined to be at 3000 rpm.

With this information, we repeat the previous calculations to find the work output and heat input of the 10HP cycle.

From the previously derived equation for the work of a cycle:

{% raw%}
$$
W_\text{cyc} = 4 \pi \tau = 4 \pi \cdot \text{24.405 Nm} = \text{306.62 J}
$$
{% endraw %}

And using the definition of thermal efficiency once more,

{% raw %}
$$
Q_\text{in} = \frac{W_\text{cyc}}{\eta} = \frac{\text{306.62 J}}{0.5711} = \text{536.89 J}
$$
{% endraw %}

We can see that the work per cycle decreased from 386.79 J to 306.62 J. The heat input per cycle decreased from 677.28 J to 536.89 J. This will result in lower fuel intake, but also a lower maximum torque output.

#### Air Intake Limitation

To make this design decision, Rehlko engineers needed to determine how much to limit the air intake to get the torque dropoff of 22.7 ft-lb to 18 ft-lb. The change in the mass of air being consumed can be determined with information we already have.

The mean effective pressure is the average pressure throughout the stroke defined by work of the cycle divided by the displacement.

{% raw %}
$$
MEP = \frac{W_\text{cyc}}{V_\text{d}}
$$
{% endraw %}

From the ideal gas law (PV=mRT), the mass of the air in the cylinder is proportional to the piston pressure under a relatively constant temperature. The mass of the air is therefore proportional to mean effective pressure. Therefore:

{% raw %}
$$
W_\text{cyc} \quad \alpha \quad  MEP \quad \alpha \quad  P \quad \alpha \quad  m_\text{air}
$$
{% endraw %}

We can simplify the work of the cycle to maximum torque since they are proportional.

{% raw %}
$$
\tau \quad  \alpha \quad MEP \quad \alpha \quad m_\text{air}
$$
{% endraw %}

This means that the ratios of torque and mass of air should be equivalent.

{% raw %}
$$
\frac{\tau_\text{10}}{\tau_\text{14}} = \frac{m\text{10 air}}{m\text{14 air}} = 0.793
$$
{% endraw %}


We can conclude that the intake should be limited such that only 79.3% of original air mass can enter the cylinder.

## Real Efficiency

Having analyzed the theoretical efficiency of the CH440 engine modified for use in Baja SAE, we now ask: how does it compare to its real performance in competition?

Thermal efficiency of a power cycle in general is expressed as

{% raw %}
$$
\eta = \frac{W_\text{cyc}}{Q_\text{in}}
$$
{% endraw %}

that is, the work produced by a cycle of work divided by the heat added during this cycle.

To calculate the amount of heat inputted, we analyze the fuel used for the engine and its lower heating value (LHV). For unleaded gasoline, the typical LHV is 12.2 kWh/kg or 43.92 MJ/kg. Baja SAE rules state all competition vehicles must use Pyrotect Part Number SFC100 as a fuel tank. The dimensions of the fuel tank are shown in the drawing (8.00 in ⌀ x 7.94 in). When full, the volume of fuel inside the tank is given by

{% raw %}
$$
V = h r^2 = (7.94)(4)^2 = 399.1 \, \text{in}^3 = 0.00654 \, \text{m}^3.
$$
{% endraw %}

<div style="display: flex; justify-content: space-between; align-items: center;">
  <img src="{{ '/assets/images/baja-fuel-tank.png' | relative_url }}" alt="First Image" style="width:48%;">
  <img src="{{ '/assets/images/baja-fuel-tank-drawing.jpg' | relative_url }}" alt="Second Image" style="width:48%;">
</div>

The typical density for unleaded gasoline is about 0.71 to 0.77 g/mL or 710 to 770 kg/m^3. To be conservative in our calculation of efficiency, we choose the highest density (i.e., a less efficient engine will need more gas to produce the same amount of work). Thus we find that the mass of gas when the gas tank is full is

{% raw %}
$$
m = \rho V = (770)(0.00654) = 5.0358 \, \text{kg}.
$$
{% endraw %}

To calculate the total heat energy that can be obtained from this amount of fuel, we use the previously mentioned LHV value to calculate

{% raw %}
$$
Q = m \cdot \text{LHV} = (5.0358) \cdot (43.92) = 221.17 \, \text{MJ}.
$$
{% endraw %}

Now the trickier part: figuring out how much work we get out of one full tank.

To do this, we will analyze Cornell's vehicle’s motion and fuel consumption during the 4-hour Baja SAE Endurance race. Looking at lap times, track length, and fuel consumption during the last Endurance Race, we find that the vehicle started the race with a full fuel tank and stopped to refuel after.

To find work, we calculate it as

{% raw %}
$$
W = F \, dl
$$
{% endraw %}

and assuming that all force is used to propel the vehicle forward, it can be reduced to

{% raw %}
$$
W = F \, l.
$$
{% endraw %}

To find the length traveled during the consumption of one full fuel tank, we look at the fact that during the most recent endurance race, Cornell’s vehicle stopped to refuel after about 2.25 hours of the endurance race. Looking at the competition’s lap logs, at this time, Cornell had completed 41 laps of the track. Given that one lap of the track at this competition measured about 1.2 miles, we find that the approximate distance traveled by the car on one fuel tank was about 49.275 miles or 79,300.4256 meters.

To find the average force exerted on the car to move it forward, we perform a static calculation. Taking the coefficient of friction between the wheel and a dirt track to be approximately

{% raw %}
$$
\mu = 0.4
$$
{% endraw %}

the free body diagram for one of the wheels looks as below:

<div style="text-align: center;">
  <img src="{{ '/assets/images/fbd-baja-wheel.png' | relative_url }}" alt="Centered Image" style="max-width:100%; height:auto;">
</div>


Multiplying the result of the friction force by four wheels, we find that the total forward force necessary to move the car forward is 889.952 N.

Going back to the work calculation, we find that the work produced by the engine using up one fuel tank is approximately

{% raw %}
$$
W = (889.952)(79,300.4256) = 70.57 \, \text{MJ}.
$$
{% endraw %}

We can finally return to the efficiency calculation to find that the real-life efficiency of the engine is approximately

{% raw %}
$$
\eta_\text{real} = \frac{70.57}{221.17} = 0.319 = 31.9\%.
$$
{% endraw %}

We find that, as would be expected, the actual efficiency is much lower than the ideal-air standard efficiency. This being said, it is more than obvious that this is not only the product of the real cycle not being ideal air (i.e., not an ideal gas but rather a fuel-air mixture, not isentropic, expansion as a result of combustion rather than heat transfer, etc.) but also due to other broader simplifying assumptions such as assuming only forward motion, assuming constant torque as average torque (when in reality the front and rear wheels produce different amounts of torque at all times and the torque varies between the transmission’s low and high-end ratios), and assuming perfect torque transmission between the wheels and ground (ignoring wheel slip and losses of energy to friction, air resistance, etc.).

<div style="text-align: center;">
  <img src="{{ '/assets/images/tg21.jpg' | relative_url }}" alt="Centered Image" style="max-width:100%; height:auto;">
</div>
