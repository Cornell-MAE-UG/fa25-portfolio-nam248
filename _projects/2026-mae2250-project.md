---
layout: project
title: MAE2250 Automated System Design
description: A comprehensive design project integrating mechanical designs and agricultural expertise
technologies: [Arduino, goBILDA Servos, Peristaltic Pumps]
image: /assets/images/Grape_Vine.jpg
---

## Table of Contents
* [Milestone 1: Client Pitch (O3)](#milestone-1-client-pitch-o3)
* [Milestone 2: Functional Prototype (O5)](#milestone-2-functional-prototype-o5)
* [Milestone 3: Client Report (06)](#milestone-3-client-report-06)

---
<div style="margin-top: 80px;"></div>

## Milestone 1: Client Pitch (O3)

**Team:** Save the Grapes  
**Client(s):** Cornell CALS Extension / E&J Gallo Winery / National Grape  

**Problem statement:**  SLFs land on grape vines and feed on their sap, contaminating harvests and resulting in grapes that taste worse for consumers. SFLs also release mold, which covers leaves, harming vine growth. A Penn State study found an average of 22.9 lantern flies on a single grape vine. When a load of juice grapes can be rejected if 1-2 adult SLF are found in a 1000-gram grape sample, sufficiently thorough on-plant removal methods can risk damaging vines. Therefore, methods to attract SLFs away from vines is more viable.

**Impact:** Grape farmers can face significant losses if their harvests are damaged or destroyed. When SLFs land on grape vines and suck their sap, plant growth is hindered, and grapes become sour. Grapes grown in regions no longer affected by spotted lantern flies would taste sweeter, farmers and consumers would not have to fear their products being contaminated by SLFs, and the price of grape products would remain stable due to increased production volume.

### Concept A: False Grape Vine

* Multiple vines would be set up throughout the vineyard with the discretion of the owner.
* These fake vines would be full of Tree of Heaven sap which SLFs prefer to the grapes as well as a 60Hz emitter which SLF are attracted to.
* Lantern flies would land and take the sap from the fake grape vine instead of real grape vines.

**Improving the Current Status Quo:**

* Farms currently spray pesticides to deter SLFs, which fade after only a few days.
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

![Average SLF per vine graph]({{ "/assets/images/figure-2-avg-of-slf-adults-per-vine.png" | relative_url }}){: style="display: block; margin: 0 auto; width: 450px;"}

<div style="text-align: center; margin-top: 15px;">
  <a href="{{ '/assets/pdfs/annotated-Save_the_Grapes.pdf' | relative_url }}" target="_blank">View Pitch PDF</a>
</div>

<div style="margin-top: 80px;"></div>

## Milestone 2: Functional Prototype (O5)

Our functional prototype for the "Save the Grapes" project is designed to attract lantern flies away from real grape vines using a simulated sap system, and then ethically dispose of them using a vinegar spray.

### Design & Assembly
[cite_start]The prototype consists of a wooden base housing the electronics and fluid reservoirs, with a central PVC pipe and a 3D-printed shower head[cite: 37, 38, 40].
* **Base Enclosure:** Constructed from $10" \times 4"$ and $8" \times 4"$ balsa wood planks. These are joined perpendicularly using 3D-printed corner attachments and M3 screws. A 3D-printed door is attached with surface-mount hinges to allow access to the internal components.
* **Fluid Routing (PVC & Tubing):** A 36-inch PVC pipe acts as the main structural stem. We routed two separate 5mm tubing lines:
    * **Inner Tubing (Vinegar):** A 43-inch line runs directly up the center of the PVC pipe and connects to the center of the 3D-printed shower head.
    * **Wrapped Tubing (Sap):** A 96-inch line exits the PVC pipe near the bottom, wraps around the exterior to simulate a vine, and re-enters near the top. Small incisions (every $1/16"$) were made in this exposed tubing using an Xacto knife to allow the "sap" to slowly leak out.

### Bill of Materials (Key Components)
The total cost for this prototype iteration was **$63.42**. The core components driving the system include:
* Kamoer NKP low-flow peristaltic pump 
* 25 feet of Soft Masterkleer PVC Tubing 
* Custom 3D-printed parts (Shower head, door, frame, brackets) 
* 12V Power Supply 
* Balsa wood paneling and M3 socket head hardware 

### Testing and Evaluation
We conducted two primary tests using water to simulate our fluids, testing the pump's ability to move fluid from the base to the top of the product:

**1. Sap Incision Flow Test**
We measured the flow rate of the liquid seeping from the wrapped tubing to verify it would act like sap. The test yielded an average flow rate of 0.5 mL/min. However, our volume scaling indicates a current drainage rate of ~180 mL/hr. 
* **Next Steps:** To meet our success criterion of $< 20$ mL/hr (allowing a 500 mL reservoir to last roughly a day), we need to slow the drive voltage from the power source or add a physical clamp to limit the flow.

**2. Vinegar Shower Head Flow Test**
This test yielded a much higher flow rate of 90 mL/min. This was expected given the larger cross-sectional area of the shower head channels compared to the tiny tubing incisions. 
* **Next Steps:** We need to physically test and verify that the spray radius exceeds 0.25m. This ensures the spray hits the lantern flies on the trap but doesn't affect actual grapes nearby. If the radius is too wide, we will redesign the shower head to cave inward like an umbrella so the spray faces the PVC pipe.

**Demonstration Day Goal:** Our primary focus for the final presentation is successfully demonstrating the $>0.25m$ vinegar spray radius. This provides a clear visual that the mechanical system works and covers the necessary area to eliminate the lantern flies.

<div style="text-align: center; margin-top: 15px;">
  <a href="{{ '/assets/pdfs/Save_The_Grapes%20Functioning%20Prototype%20Write%20Up-1.pdf' | relative_url }}" target="_blank">View Functional Prototype PDF</a>
</div>

<div style="margin-top: 80px;"></div>

## Milestone 3: Client Report (06)

**Neil Morrison, Susanna Aufrichtig, Jamie Dalvito, Flavia Capet, and Luca Welle**

![VineGuard CAD Render]({{ "/assets/images/Rough Assembly_1.png" | relative_url }}){: style="display: block; margin: 0 auto; width: 100%; max-width: 600px;"}

### Context and Problem Statement
Spotted Lanternflies (SLFs), an invasive species rapidly spreading across the eastern United States, pose a growing threat to agricultural systems. SLFs land on grape vines and feed on plant sugars, contaminating harvests, reducing yields, and worsening grapes. SFLs also excrete honeydew, promoting growth of sooty mold that inhibits photosynthesis. These effects can cost the wine industry billions of dollars in lost yields. 

On-vine SLF removal was shown to be impractical because the insects are numerous, and aggressive removal methods could damage the vines. Post harvest removal proved to be too risky considering the high rate of contamination. So instead, we wondered if there was a way to attract SFLs away from the vines completely.

### Final Prototype and Application
To lure SLFs away from grapevines, our system utilizes a sugary attractant designed to mimic the sap of the Tree of Heaven, a preferred host plant. Once lured to the device, SLFs are then exterminated using targeted vinegar spraying through side-mounted sprayers.

1. **Sap Attraction:** We pump a sugar solution that mimics the viscosity of natural sap through a central pole, creating an attractive feeding source.
2. **Targeted Elimination:** Once the insects gather, we spray them with vinegar using servo-actuated sprayers.

**Key features:**
1. Adjustable spray angles for coverage optimization
2. Compact footprint for vineyard integration
3. Arduino-controlled automation
4. Low-toxicity vinegar-based treatment

A vineyard simply places the device, turns it on, and it runs autonomously with minimal maintenance.

### Assembly
The system is designed so the box exterior can be rapidly assembled or disassembled if need be. Each panel contains a lip to maintain box geometry. Screws are then attached throughout each panel for rigidity. The lid of the box consists of two pieces which are loosely pressed to fit to the top of the box, giving quick access to the interior electronics and fluid reservoirs for maintenance. 

One of the panels contains a mounting profile for the electrical board which is held on with four screws on the interior of the box. Electrical components are wired together using jumper wires and Wago connectors which can be plugged directly into the arduino and allow for easily connecting components in parallel. 

A 3D printed linkage allows servo motors to actuate the sprayer heads. A 3D printed bar is screwed into the servo horn which pulls the actuator forwards and backwards. Everything is then rigidly attached together using screws and mounted on the top box panel.

### Testing Details and Results

#### 1. Sap Drainage Test
To test the longevity of our sap reservoir, we conducted a drainage test to determine how long the system could realistically last in the field without being refilled.
* **Procedure:** Mix 200 g sucrose + 300 g water to mimic Tree of Heaven sap viscosity (~5 mPa*s). Pump solution for 10 min, recording water level every 2.5 min.
* **Results:** Drainage rate: 0.5 mL/min (6mL/day) -> 1000mL reservoirs must be refilled every ~167 days.

#### 2. Spray Angle & Coverage
To confirm that our sprayers could cover the majority of the central pole in vinegar, we tested sprayer angles to find max coverage.
* **Procedure:** Cover central pole in paper, set sprayers to a specific angle, perform a spraying cycle, measure area of paper that is damp.
* **Results:** The optimal working angle of the sprayers was found to be 65 degrees, achieving 86% spray coverage. This allows for most coverage of the landing area of the SLF on our system.

#### 3. Battery Life
To evaluate VineGuard's power constraints, we calculated energy consumption. VineGuard can operate for approximately 8.2 days on a 10,000mAh battery charge. The system's modular battery design enables users to balance cost against serviceability depending on deployment needs.

**Power Consumption & Battery Life**

| Component | Current Draw (Active) (mA) | Active Time (hr/day) | Current Draw (Idle) (mA) | Idle Time (hr/day) | Daily Consumption (mAh/day) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Pump** | 300 | 0.2 | 0 | 0 | 60 |
| **Servo** | 800 | 0.006 | 8 | 23.994 | 200.9 |
| **Arduino** | 40 | 24 | - | - | 960 |
| **Total** | | | | | **1220.9** |

**Battery Performance**

| Parameter | Value |
| :--- | :--- |
| Battery Capacity | 10,000 mAh |
| Daily Usage | 1220.9 mAh |
| Battery Life | 8.2 days |

### Conclusion and Recommendation
Based on our test results, Vineguard demonstrates a strong potential as a feasible and effective solution for protection against SFLs. Our testing showed that the system can deliver the attractant at controlled flow rates, achieve ideal spray coverage under specific angles, and operate for around 167 days completely autonomously based on power supply. Additionally, the manufacturing and assembly process required minimal setup, and the system showed low maintenance demands once built. 

Given this performance we would recommend development of our prototype to move forward with field testing as the next step. It will be important to test the attractant that will be used, along with ideal placement that will bring in the most insects at a time. Also, taking tourism into account is important so the aesthetics of the design would also need to be modified to camouflage it into the vineyard as much as possible. 

Overall, VineGuard offers a feasible low-toxicity, low-intervention solution for mitigating SLF damage in vineyards through a bio-inspired decoy system. This prototype has the potential to not only save vineyards millions in yields but also to provide an eco-friendly, passive, low maintenance solution compared to past pest control methods.

### BOM for Final Prototype

| Description | Vendor | McMaster Code | Quantity | Unit of measurement | Total Cost |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Soft Masterkleer PVC Tubing for Air and Water | McMaster Carr | 5233K113 | 1 | 25 feet | $11.50 |
| Push to Connect Fitting | McMaster Carr | 3619N12 | 6 | Pack of 1 Each | $15.66 |
| Kamoer NKP low flow peristaltic pump | Amazon | | 1 | Pack of 1 | $9.98 |
| M3x0.5 Black-Oxide Alloy Steel Socket Head Screw 14mm Long | McMaster Carr | 91290A119 | 1 | Pack of 1 | $15.30 |
| 12V Power Supply | Taylor Design Studio | | 1 | Pack of 1 | $6.99 |
| Metal Servo Arms Horn | Amazon | | 1 | Pack of 6 | |
| Arduino Uno REV3 | Amazon | | 1 | Pack of 1 | $27.60 |
| L298N Motor Driver | Amazon | | 1 | Pack of 2 | $6.98 |
| LM2596 DC to DC Buck Converter | Amazon | | 1 | Pack of 5 | $7.99 |
| Wago 221-415 Lever-Nuts | Amazon | | 1 | Pack of 10 | $9.85 |
| Round Rocker Switches | Amazon | | 1 | Pack of 5 | $6.39 |
| Spray Bottle Long-Reach, 1 Gallon Capacity | McMaster Carr | 9864T16 | 2 | Pack of 1 | $8.80 |
| Routing Clamp 304 Stainless Steel, 2 Mounting Points, 15/16" ID | McMaster Carr | 8874T43 | 2 | Pack of 1 | $7.42 |
| Semi-Clear HDPE Plastic Bottle 32 FL. oz./1000 ml Capacity, 1-1/2" Mouth OD | McMaster Carr | 3681T77 | 2 | Pack of 1 | $7.46 |
| 2000 Series 5-Turn, Dual Mode Servo | Taylor Design Studio | | 1 | Pack of 1 | |
| Black-Oxide Alloy Steel Socket Head Screw M3x0.5 mm Thread Size, 40 mm Long | McMaster Carr | | 1 | Pack of 25 | $4.86 |
| Zinc-Plated Steel Hex Nut Medium-Strength, ISO Class 8, M3 x 0.5mm Thread Size | McMaster Carr | 90591A250 | 1 | Pack of 100 | $3.06 |
| **Total Cost** | | | | | **$149.84** |

### Works Cited
1. Amdro, "How to control and kill spotted lanternflies." Available: Amdro website.
2. CNBC, "Spotted lanternflies are feasting on U.S. grapevines and putting vineyards at risk," Oct. 13, 2022.
3. Cornell Chronicle, "Spotted lanternflies could cost NYS grape industry millions," Jan. 27, 2025.
4. BioNumbers (BNID 108683), "Viscosity of the sap (typically ~5× water)," Harvard Medical School.
5. Penn State Extension, "Spotted lanternflies and beekeeping," Oct. 5, 2025.

<div style="text-align: center; margin-top: 15px;">
  <a href="{{ '/assets/pdfs/Open%20Design%20Project%206_%20Exhibit%20and%20Client%20Report.pdf' | relative_url }}" target="_blank">View Final Client Report PDF</a>
</div>