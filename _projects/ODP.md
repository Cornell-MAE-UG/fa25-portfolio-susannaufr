---
layout: project
title: MAE2250 Open Design Project
description: Class Assignment
image: /assets/images/SLF-Adult_on_grapes.jpg
technologies:
  - Written Report
---
# MAE2250 Open Design Project
---

## Table of Contents

- [Client Outline](#client-outline)
- [Functioning Prototype](#functioning-prototype)
- [Client Report](#client-report)

---

# Client Outline
<a id="client-outline"></a>

## Grapevine Redirection and Attraction for Pest Elimination

**Team:** Save the Grapes
**Client(s):** Cornell CALS Extension / E\&J Gallo Winery / National Grape  

**Problem statement:**  SLFs land on grape vines and feed on their sap, contaminating harvests and resulting in grapes that taste worse for consumers. SFLs also release mold, which covers leaves, harming vine growth. A Penn State study found an average of 22.9 lantern flies on a single grape vine. When a load of juice grapes can be rejected if 1-2 adult SLF are found in a 1000-gram grape sample, sufficiently thorough on-plant removal methods can risk damaging vines. Therefore, methods to attract SLFs away from vines is more viable.

**Impact:** Grape farmers can face significant losses if their harvests are damaged or destroyed. When SLFs land on grape vines and suck their sap, plant growth is hindered, and grapes become sour. Grapes grown in regions no longer affected by spotted lantern flies would taste sweeter, farmers and consumers would not have to fear their products being contaminated by SLFs, and the price of grape products would remain stable due to increased production volume.

### Concept A: False Grape Vine

* Multiple vines would be set up throughout the vineyard with the discretion of the owner

* These fake vines would be full of Tree of Heaven sap which SLFs prefer to the grapes as well as a 60Hz emitter which SLF are attracted to 

* Lantern flies would land and take the sap from the fake grape vine instead of real grape vines

**Improving the Current Status Quo:**

* Farms currently spray pesticides to deter SLFs, which fade after only a few days

* No interference with existing growing processes. The traps do not touch the grape vines.

**End-of-semester proof-of-concept:** One single vine made from 3D prints, wood, and purchased parts, 60Hz emitter, and liquid to simulate Tree of Heaven sap.

### Key risks

* **Risk 1** — Faux grape vine traps may occupy usable growing space in vineyards. We will test how the product's size changes its effectiveness by altering variables such as trap size, sap potency, and vibration frequency.

* **Risk 2** — The vine may attract unwanted insects or animals to the vineyards, so we will monitor the trap at the site before full implementation.

### Questions for the client
1. How much space does the client have available for the traps on the farm? This will determine the size of our final product and where it can be implemented.

2. What are the dimensions of an average vineyard/ (rows, terrain, trellises, etc.)? This will help us determine the best way to integrate our trap with each farm.

3. Are there any regulations you think we should be aware of? This provides us design constraints and keeps us aware of the environmental impact of our design.

## References

- **Source 1** https://www.canr.msu.edu/resources/a-tale-of-two-invaders-tree-of-heaven-and-spotted-lanternfly
- **Source 2** https://extension.psu.edu/spotted-lanternfly-management-in-vineyards

## Figure

<div style="text-align: left;">
  <img src="{{ '/assets/images/figure-2-avg-of-slf-adults-per-vine.png' | relative_url }}" alt="Lantern Fly Density on Grape Vines" style="max-width:100%; height:auto;">
</div>

---

# Functioning Prototype
<a id="functioning-prototype"></a>

---

**Design Documentation**

**Design Intent:**

Sketch:
<div style="text-align: center;">
  <img src="{{ '/assets/images/I2.png' | relative_url }}" style="max-width:80%; height:auto;">
</div>  
CAD Assembly:
<div style="text-align: center;">
  <img src="{{ '/assets/images/I3.png' | relative_url }}" style="max-width:80%; height:auto;">
</div>

**Assembly Process:**

**Box Base:**

* Materials:  
  * Balsa Wood  
  * 3D printed door and door frame  
  * 28 Screws  
    * 56 Washers  
    * 28 Hex nuts  
  * 2 3D printed top attachments  
  * 8 Corner attachments  
  * 2 Hinges  
  * Hand Saw  
  * Hole Saw  
* Measurements:  
  * Long sides & Top pieces: 10in x 4in  
  * Back & Front: 8in x 4in  
* Assembly:  
  * Cut four balsa planks to 10in using hand saw  
  * Cut one plank to 8in using hand saw  
  * Attach two 10in pieces parallel using 4 screws and the two 3d printed top attachments to create the top  
  * Connect a top plank to a side plank perpendicularly with the corner attachment   
    * Insert screw with a washer on each side and secure with nut  
    * Two of these corner attachments per side  
    * Corner attachments should be always connected to a top piece   
  * Repeat this step until it is a box without a front or a bottom  
    * All pieces should be connected to the top  
  * Take 3D printed frame and attach in the same way using corner attachments  
  * Use hinges to attach 3D printed door to the frame  
    * Attach with screws, washers, and nuts  
  * Cut hole through the middle using a hole saw

**PVC Pipe & Tubing:**

* Materials:  
  * 25 ft Plastic 5mm tubing  
  * 3d printed shower head  
  * PVC Pipe  
  * Tape  
  * Xacto Knife  
  * Dremel  
* Measurements:  
  * Inner Tubing (Vinegar): 43 in  
  * Wrapped Tubing (Sap): 96 in  
  * PVC Pipe: 36 in  
* Assembly:  
  * Dremel hole in PVC Pipe 4.5in up from the bottom for wrapped tubing to exit out of  
  * Dremel hole in PVC pipe 1.5 in from top for wrapped piping to go back inside  
  * Dremel hole 2 in from the bottom of PVC pipe  
  * Cut the 25 ft plastic 5mm tubing into one 43in piece (inner) and one 96 in piece (wrapped)  
  * Run inner tubing through middle of PVC pipe and connect to the smallest hole in the center of the shower head  
    * Secure with tape  
  * Exit it on the bottom through the hole 2in from bottom  
  * Run wrapped tubing through the bottom of the PVC pipe and out the first hole(4.5in from bottom)  
  * Wrap the tubing around the pvc pipe until the hole at the top  
    * Secure with tape  
  * Push tubing through the hole and the top and back down the pipe but through the center now and exit it at the hole 2 in from the bottom  
  * Place PVC Pipe with wrapped tubing through hole in the box  
  * Go through and every 1/16 in make a very small slash in the wrapped tubing outside using the Xacto knife

**Design Test**

Our testing process verified two different aspects of our prototype, both of which involved the pumping of water from the base to the top of the product. Water was used as the test fluid due to its accessibility and similar qualities to our final fluid we will use. Our first test examined fluid flow from the pump out of the tubing that wrapped around the PVC pipe. We used an Xacto knife to make small incisions in the tubing to enable water to flow out of it. These incisions will closely, if not exactly, reflect how we will create holes in our final product. We measured incision flow in time intervals of 2.5 mins due to our assumption that the flow rate would be very small, which would make it difficult to measure the flow rate on a seconds based time interval. Also, we chose minutes as our time scale because we intend to have the fluid in the final product last several days before being refilled. We were unable to measure on a time scale of hours because our lab time did not allow for it. We used a measuring device graduated in 10 mL increments when measuring flow rates.

**Data Table 1** shows our results from the incision flow. Based on **Data Table 1**, our average flow rate was 3 mL/min, confirming our assumption that incision flow would be very small. **Image 1** shows the water that was used in the tube and coming out of the tube, which confirmed a part of our success criteria. 

| Incision Flow |  |
| ----- | ----- |
| 0 | 400 |
| 2.5 | 390 |
| 5 | 385 |
| 7.5 | 380 |
| 10 | 370 |
|  |  |
| Flow Rate Initial \- Final(Avg mL/min) | 3 |


<div style="text-align: center;">
  <img src="{{ '/assets/images/I4.png' | relative_url }}" alt="Image 1" style="max-width:100%; height:auto;">
</div>

**Data Table 2** shows the results from the flow rate from the shower head design experiment. The flow rate for the shower head design was noticeably higher than the incision design (factor of 30x). This matched our expectations because we had a much larger cross sectional area in the shower head for the water to flow when compared with the incision design. **Image 2** shows the shower head design experiment. We propped the shower head at a height similar to where it would stand on the final product in order to gauge flow rate at a non-zero height above the pump. This is important because the higher the water has to be pumped, the slower the flow rate will be. 

| Time (min) | ml |
| ----- | ----- |
| 0 | 370 |
| 0.5 | 320 |
| 1 | 300 |
| 1.5 | 250 |
| 2 | 200 |
| 2.5 | 150 |
| 3 | 100 |
|  |  |
| Flow Rate (mL/min) | 90 |

<div style="text-align: center;">
  <img src="{{ '/assets/images/I5.png' | relative_url }}" alt="Image 2" style="max-width:100%; height:auto;">
</div>


**Success Criteria**

**Context:** We are looking to create a fake grape vine to attract lantern flies away from vineyards so they don’t destroy real grape vines. Once we have attracted the lantern flies away from the real grape vines, we are then able to ethically dispose of them. 

Looking at the next step in our timeline which is refining some of our tests and design from this prototype. With that we noticed a couple of issues in our current tests that could be refined.

**Project Success Criteria**

1)  **Sap Fluid Drainage at a rate \< 20mL/hr**

   Since our sap slowly leaks out of the holes along the wrapped tubing we want to make sure that it doesn’t drain out too quickly, in order to save the maintenance time of refilling. Looking at our data right now we have a drainage rate of around 180ml/hr for the sap so we definitely want to cut that down in the future. To do this we would have to slow the drive voltage from the power source or we could try out a clamp on one of the ends to limit the flow down. If we have the flow at 20 ml an hour the sap would need to be replaced around once a day considering a 500 ml reservoir at the bottom. This could easily be tested again using our pup and tracking volume. This is in representation of our smaller scaled model so it would probably be around once a week for the larger “real world” model when scaled up.

 


2)  **Vinegar Sprayer Spraying Radius of \>0.25m**

   When thinking about our concept we wanted to make sure that our vinegar doesn’t really spray anything but the distraction so that it wouldn't affect the grapes. With that we want to make sure that our radius is limited to 0.25m. We did not measure radius this time so it will be interesting to see what our next set of tests shows. The radius could be measured by placing a paper underneath our contraption and running the shower system for around 30 seconds and see where the farthest droplet lands on the paper underneath. In terms of design criteria to maximize this We could redesign our shower head to cave inward like an umbrella so the spray faces the PVC pipe.

3)  **Electronics and Fluid Storage Contained within a 320 cubic inches Volume**

   We have limited space for the reservoirs in the boxes underneath so both the vinegar and sap reservoirs along with the electronics have to fit. For this we would have to maximize the fluid storages while still prioritizing the safety of the electronics. 

   

**Demonstration Day Criteria** 

When it comes to demonstration day criteria, one of the most relevant is the success of the vinegar sprayer spraying radius being greater than 0.25m. This is because it is a clear visual for those in the audience that we were able to get a key mechanical system working but also that we would be able to kill lantern flies in a wide area which are on our system.

---

# Client Report 
<a id="client-report"></a>


**Context and Problem Statement**  
Spotted Lanternflies (SLFs), an invasive species rapidly spreading across the eastern United States, pose a growing threat to agricultural systems.2 SLFs land on grape vines and feed on plant sugars, contaminating harvests, reducing yields, and worsening grapes.2 SFLs also excrete honeydew, promoting growth of sooty mold that inhibits photosynthesis.5 These effects can cost the wine industry billions of dollars in lost yields.3 On-vine SLF removal was shown to be impractical because the insects are numerous, and aggressive removal methods could damage the vines. Post harvest removal proved to be too risky considering the high rate of contamination. So instead, we wondered if there was a way to attract SFLs away from the vines completely.

**Final Prototype and Application**  
To lure SLFs away from grapevines, our system utilizes a sugary attractant designed to mimic the sap of the Tree of Heaven, a preferred host plant5. Once lured to the device, SLFs are then exterminated using targeted vinegar1 spraying through side-mounted sprayers.

**1\. Sap Attraction:** We pump a sugar solution that mimics the viscosity of natural sap through a central pole, creating an attractive feeding source.  
**2\. Targeted Elimination:** Once the insects gather, we spray them with vinegar using servo-actuated sprayers.

Key features:

1) Adjustable spray angles for coverage optimization  
2) Compact footprint for vineyard integration  
3) Arduino-controlled automation  
4) Low-toxicity vinegar-based treatment

**A vineyard simply places the device, turns it on, and it runs autonomously with minimal maintenance.**
<div style="text-align: left;">
  <img src="{{ '/assets/images/pA' | relative_url }}"  style="max-width:60%; height:auto;">
</div>
<div style="text-align: left;">
  <img src="{{ '/assets/images/pB' | relative_url }}"  style="max-width:60%; height:auto;">
</div>
**Assembly**  
The system is designed so the box exterior can be rapidly assembled or disassembled if need be. Each panel contains a lip to maintain box geometry. Screws are then attached throughout each panel for rigidity. The lid of the box consists of two peices which are loosely pressed to fit to the top of the box, giving quick access to the interior electronics and fluid reservoirs for maintenance. One of the panels contains a mounting profile for the electrical board which is held on with four screws on the interior of the box. Electrical components are wired together using jumper wires and Wago connectors which can be plugged directly into the arduino and allow for easily connecting components in parallel. A 3D printed linkage allows servo motors to actuate the sprayer heads. A 3D printed bar is screwed into the servo horn which pulls the actuator forwards and backwards. Everything is then rigidly attached together using screws and mounted on the top box panel.
<div style="text-align: left;">
  <img src="{{ '/assets/images/pC' | relative_url }}"  style="max-width:60%; height:auto;">
</div>
<div style="text-align: left;">
  <img src="{{ '/assets/images/pD' | relative_url }}"  style="max-width:60%; height:auto;">
</div>
<div style="text-align: left;">
  <img src="{{ '/assets/images/pE' | relative_url }}"  style="max-width:60%; height:auto;">
</div>
<div style="text-align: left;">
  <img src="{{ '/assets/images/pF' | relative_url }}"  style="max-width:60%; height:auto;">
</div>

**Testing Details and Results**

1. **Sap Drainage Test:** To test to longevity of our sap reservoir, we conducted a drainage test to determine how long the system could realistically last in the field without being refilled

**Procedure:**

1) Mix 200 g sucrose \+ 300 g water to mimic Tree of Heaven sap viscosity (\~5 mPa·s) 4  
2) Pump solution for 10 min, recording water level every 2.5 min

**Results:**

<div style="text-align: middle;">
  <img src="{{ '/assets/images/pG' | relative_url }}"  style="max-width:60%; height:auto;">
</div>

* Drainage rate: 0.5 mL/min  (6mL/day) → 1000mL reservoirs must be refilled every \~167 da**2\.   Spray Angle & Coverage:** To confirm that our sprayers could cover the majority of the central pole in vinegar, we tested sprayer angles to find max coverage.

**Procedure:**

1) Cover central pole in paper, set sprayers to a specific angle, perform a spraying cycle, measure area of paper that is damp

**Results:**

* The optimal working angle of the sprayers was found to be 65 degrees, achieving 86% spray coverage. This allows for most coverage of the landing area of the SLF on our system

**3\. Battery Life**  
To evaluate VineGuard’s power constraints, we calculated energy consumption.

**Results:**

* VineGuard can operate for approximately 8.2 days on a 10,000mAh battery charge. The system’s modular battery design enables users to balance cost against serviceability depending on deployment needs.

**Conclusion and Recommendation**

Based on our test results, Vineguard demonstrates a strong potential as a feasible and effective solution for protection against SFLs. Our testing showed that the system can deliver the attractant at controlled flow rates, achieve ideal spray coverage under specific angles, and operate for around 167 days completely autonomously based on power supply. Additionally, the manufacturing and assembly process required minimal setup, and the system showed low maintenance demands once built. Given this performance we would recommend development of our prototype to move forward with field testing as the next step. It will be important to test the attractant that will be used, along with ideal placement that will bring in the most insects at a time. Also, taking tourism into account is important so the aesthetics of the design would also need to be modified to camouflage it into the vineyard as much as possible. Overall, Vinegaurd offers a feasible low-toxicity, low-intervention solution  for mitigating SLF damage in vineyards through a bio-inspired decoy system. This prototype has the potential to not only save vineyards millions in yields but also to provide an eco-friendly, passive, low maintenance solution compared to past pest control methods.  
**BOM for Final Prototype:**

| Description | Vendor | McMaster Code | Quantity | Unit of measurement | Total Cost |
| ----- | ----- | ----- | :---: | :---: | :---: |
| Soft Masterkleer PVC Tubing for Air and Water | McMaster Carr | 5233K113 | 1 | 25 feet | $11.50 |
| Push to Connect Fitting | McMaster Carr | 3619N12 | 6 | Pack of 1 Each | $15.66 |
| Kamoer NKP low flow peristaltic pump | Amazon |  | 1 | Pack of 1 | $9.98 |
| M3 x 0.5 Black-Oxide Alloy Steel Socket Head Screw 14mm Long  | McMaster Carr | 91290A119  | 1 | Pack of 1 | $15.30 |
| 12V Power Supply | Taylor Design Studio |  | 1 |  | \~ |
|  Metal Servo Arms Horn Aluminum | Amazon |  | 1 | Pack of 6 | $6.99 |
| Arduino Uno REV3 | Amazon |  | 1 | Pack of 1 | $27.60 |
| L298N Motor Driver | Amazon |  | 1 | Pack of 2 | $6.98 |
| LM2596 DC to DC Buck Converter | Amazon |  | 1 | Pack of 5 | $7.99 |
| Wago 221-415 Lever-Nuts  | Amazon |  | 1 | Pack of 10 | $9.85 |
| Round Rocker Switches | Amazon |  | 1 | Pack of 5 | $6.39 |
| Spray Bottle Long-Reach, 1 Gallon Capacity | McMaster Carr | 9864T16 | 2 | Pack of 1 | $8.80 |
| Routing Clamp 304 Stainless Steel, 2 Mounting Points, 15/16" ID | McMaster Carr | 8874T43 | 2 | Pack of 1 | $7.42 |
| Semi-Clear HDPE Plastic Bottle 32 FL. oz./1000 ml Capacity, 1-1/2" Mouth OD | McMaster Carr | 3681T77 | 2 | Pack of 1 | $7.46 |
| 2000 Series 5-Turn, Dual Mode Servo | Taylor Design Studio |  | 1 |  | \~ |
| Black-Oxide Alloy Steel Socket Head Screw M3 x 0.5 mm Thread Size, 40 mm Long | McMaster Carr |  | 1 | Pack of 25 | $4.86 |
| Zinc-Plated  Steel Hex Nut Medium-Strength, ISO Class 8, M3 x 0.5mm Thread Size  | McMaster Carr | 90591A250 | 1 | Pack of 100 | $3.06 |
| **Total Cost** |  |  |  |  | $149.84 |

**Works Cited**  
\[1\] Amdro, “How to control and kill spotted lanternflies.” Available: Amdro website.  
\[2\] CNBC, “Spotted lanternflies are feasting on U.S. grapevines and putting vineyards at risk,” Oct. 13, 2022\.  
\[3\] Cornell Chronicle, “Spotted lanternflies could cost NYS grape industry millions,” Jan. 27, 2025\.  
\[4\] BioNumbers (BNID 108683), “Viscosity of the sap (typically \~5× water),” Harvard Medical School.  
\[5\] Penn State Extension, “Spotted lanternflies and beekeeping,” Oct. 5, 2025\.

