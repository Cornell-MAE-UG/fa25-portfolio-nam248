---
layout: project
title: MAE2250 Automated System Design
description: A comprehensive design project integrating mechanical designs and argicultural expertise
technologies: [Arduino, goBILDA Servos, Paristaltic Pumps]
image: /assets/images/Grape_Vine.jpg
---

## Table of Contents
* [Milestone 1: Client Pitch (O3)](#milestone-1-client-pitch-o3)
* [Milestone 2: Functional Prototype (O5)](#milestone-2-functional-prototype-o5)
* [Milestone 3: Client Report](#milestone-3-client-report)

---

## Milestone 1: Client Pitch (O3)


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

![Average SLF per vine graph]({{ "/assets/images/figure-2-avg-of-slf-adults-per-vine.png" | relative_url }}){: style="display: block; margin: 0 auto; width: 450px;"}

<div style="text-align: center; margin-top: 15px;">
  <a href="{{ '/assets/pdfs/annotated-Save_the_Grapes.pdf' | relative_url }}">View Pitch PDF</a>
</div>

<div style="margin-top: 80px;"></div>

## Milestone 2: Functional Prototype (O5)

Our functional prototype for the "Save the Grapes" project is designed to attract lantern flies away from real grape vines using a simulated sap system, and then ethically dispose of them using a vinegar spray.

### Design & Assembly
The prototype consists of a wooden base housing the electronics and fluid reservoirs, with a central PVC pipe and a 3D-printed shower head[cite: 37, 38, 40].
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

[View Functional Prototype PDF]({{ "/assets/pdfs/Save_The_Grapes Functioning Prototype Write Up-1.pdf" | relative_url }})

## Milestone 3: Client Report

### Proposed Solution & Prototype
[Describe the final design choice and the physical build of the system.]

### How It Works / Is Used
[Explain the operational flow—e.g., how the system takes input commands and translates them through the microcontroller into physical action via the servos and linear actuators.]

### Conclusion
[Summarize the results, performance against design constraints, and overall success of the build.]

### Recommendation for Next Steps
[Discuss future iterations, alternative parts, or scaling the project.]