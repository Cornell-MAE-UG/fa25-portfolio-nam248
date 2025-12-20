---
layout: project
title: Thermodynamic Device Analysis
description: Device Analysis
technologies: [Autodesk Fusion]
image: /assets/images/LimerickPowerPlant.jpg
---

Close to my home in Phildalphia, there is a nuclear power plant around fifty miles north of the city kno wn as Limerick Generating Station. This is a nuclear power plant that provides power to roughly 1.7 million homes in the surrounding area. In this breif project, I will be describing a couple of the devices used in this power plant to generate energy for the surrounding area, well as analyzing the efficiencies of these devices to get a sense for how well this nuclear power plant extracts energy. 

The Limerick Power Plant is known as a boiling water reactor. This is where heat from a fission reaction is taken up by water in the reactor vessel and turning it into steam. This superheated steam is then directed to a turbine generator which converts energy from the steam into electrical power. The thermodynamic cycle used in this case is a Rankine Cycle which utilizes a turbine to do work, a condenser to reject heat, a pump requiring work to pump liquid water back to pressure, and a boiler to add heat. 


![Shaded rendering of earlier version]({{ "/assets/images/bwr_reactor.png" | relative_url }}){: .inline-image-r style="width: 200px"}
![Shaded rendering of earlier version]({{ "/assets/images/brayton_cycle.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}


In this anaylsis, I will be primarily looking at two devices used in the Limerick Power Plant: the reactor boiler and the turbine. To find data at different states in the Limrick Rankine Cycle, I primarily used the [U.S.NRC Generic Environmental Impact Statement for License Renweal of Nuclear Plants Report](https://www.nrc.gov/reading-rm/doc-collections/nuregs/staff/sr1437/r1/index). This is where I found values for the mass flowrate of the reactor. I also used common pressure and tempurature values found in BWR reactors from [The International Atomic Energy Agency](https://www-pub.iaea.org/MTCD/Publications/PDF/TCS-23_2nd_web.pdf) so I could calculate the Work and Heat of these devices. Specifically what I will be finding from the turbine and the boiler is the Heat added from the boiler, the Work output of the turbine, the efficiency of the plant, and then the isentropic efficiency of the turbine. I will then compare these calculated efficiences to the real efficiences of BWR reactors. 


First, to state some assumptions before analyzing these devices, I am going to assume that the turbine is adiabatic and that the Kinetic and Potenial Energy changes of this cycle are negligible beacuse the enthalpy changes from state to state are so massive. Heat addition also takes place at constant pressure like in an ideal Rankine Cycle. To start, we can see that the given value for the mass flow rate through the condenser from the U.S.NRC document is 450,000 gpm, this roughly converts to:

$$
\dot{m} = 28390\ \text{kg/s}
$$

Finding 
$$ 
\dot{Q_in}
$$
for the Boiler

Given 

Boiler Pressure : $P_b = 7.0\ \text{MPa}$
Boiler Inlet Temperature : $T_i = 215\ \text{C}$
Boiler Outlet Temperature (Turbine Inlet Tempurature): $T_o = 290\ \text{C}$

We can use the first law for a control volume 

$$
\dot{E} = \dot{Q} - \dot{W} + \sum_{}\dot{m}h_i - \sum_{}\dot{m}h_o
$$


aaaa