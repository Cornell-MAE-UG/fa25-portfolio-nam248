---
layout: project
title: MAE2250 Automated System Design
description: A comprehensive design project integrating mechanical systems and vineyard protection
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

\newpage

## References

- **Source 1** https://www.canr.msu.edu/resources/a-tale-of-two-invaders-tree-of-heaven-and-spotted-lanternfly
- **Source 2** https://extension.psu.edu/spotted-lanternfly-management-in-vineyards

## Figure
![Shaded rendering of earlier version]({{ "/assets/images/figure-2-avg-of-slf-adults-per-vine.png" | relative_url }}){: .inline-image-r style="width: 300px"}





[View Pitch PDF](/assets/pdfs/annotated-Save_the_Grapes.pdf)

## Milestone 2: Functional Prototype (O5)
[Insert details about your prototype here. This is a great place to drop in photos of your hardware setup, CAD models, or wiring diagrams showing how your Arduino interfaces with your motor drivers and actuators.]

## Milestone 3: Client Report

### Proposed Solution & Prototype
[Describe the final design choice and the physical build of the system.]

### How It Works / Is Used
[Explain the operational flow—e.g., how the system takes input commands and translates them through the microcontroller into physical action via the servos and linear actuators.]

### Conclusion
[Summarize the results, performance against design constraints, and overall success of the build.]

### Recommendation for Next Steps
[Discuss future iterations, alternative parts, or scaling the project.]