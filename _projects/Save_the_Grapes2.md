---
layout: project
title: MAE 2250 ODP Functional Prototype
description: Class Assignment
image: /assets/images/I1.png
technologies:
  - Written Report
---

# ODP 4: Functioning Prototype**

**Save the Grapes : Neil, Susanna, Jamie, Flavia, and Luca**

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

