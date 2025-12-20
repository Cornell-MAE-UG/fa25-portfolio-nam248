---
layout: project
title: Limerick Power Plant Rankine Cycle Analysis
description: Device Analysis
technologies: [Autodesk Fusion]
image: /assets/images/LimerickPowerPlant.jpg
---

Close to my home in Phildalphia, there is a nuclear power plant around fifty miles north of the city kno wn as Limerick Generating Station. This is a nuclear power plant that provides power to roughly 1.7 million homes in the surrounding area. In this breif project, I will be describing a couple of the devices used in this power plant to generate energy for the surrounding area, well as analyzing the efficiencies of these devices to get a sense for how well this nuclear power plant extracts energy. 

The Limerick Power Plant is known as a boiling water reactor. This is where heat from a fission reaction is taken up by water in the reactor vessel and turning it into steam. This superheated steam is then directed to a turbine generator which converts energy from the steam into electrical power. The thermodynamic cycle used in this case is a Rankine Cycle which utilizes a turbine to do work, a condenser to reject heat, a pump requiring work to pump liquid water back to pressure, and a boiler to add heat. 


![Shaded rendering of earlier version]({{ "/assets/images/bwr_reactor.png" | relative_url }}){: .inline-image-r style="width: 200px"}
![Shaded rendering of earlier version]({{ "/assets/images/brayton_cycle.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}


In this anaylsis, I will be primarily looking at two devices used in the Limerick Power Plant: the reactor boiler and the turbine. To find data at different states in the Limrick Rankine Cycle, I primarily used the [U.S.NRC Generic Environmental Impact Statement for License Renweal of Nuclear Plants Report](https://www.nrc.gov/reading-rm/doc-collections/nuregs/staff/sr1437/r1/index). This is where I found values for the mass flowrate of the reactor. I also used common pressure and tempurature values found in BWR reactors from [The International Atomic Energy Agency](https://www-pub.iaea.org/MTCD/Publications/PDF/TCS-23_2nd_web.pdf) so I could calculate the Work and Heat of these devices. Specifically what I will be finding from the turbine and the boiler is the Heat added from the boiler, the Work output of the turbine, the efficiency of the plant, and then the isentropic efficiency of the turbine. I will then compare these calculated efficiences to the real efficiences of BWR reactors. 


## Assumptions

First, to state some assumptions before analyzing these devices, I am going to assume that the turbine is adiabatic and that the Kinetic and Potenial Energy changes of this cycle are negligible beacuse the enthalpy changes from state to state are so massive. Heat addition also takes place at constant pressure like in an ideal Rankine Cycle and all devices are in steady state. To make things clear, when going around this cycle to find specific values, I am going to call the Boiler Inlet state (1), the Turbine Inlet state (2), and the Condenser Inlet state (3). In the basic rankine cycle, this goes:

Boiler → Turbine → Condenser → Pump

### Given

To start, we can see that the given value for the mass flow rate through the condenser from the U.S.NRC document is 450,000 gpm, this roughly converts to:
$\dot{m}$
$ = 28390\ \text{kg/s}$

We also have values for: 

Boiler Pressure : $P_1 = 7.0\ \text{MPa}$

Boiler Inlet Temperature : $T_1 = 215\ \text{C}$

Boiler Outlet Temperature (Turbine Inlet Tempurature): $T_2 = 290\ \text{C}$

## Boiler Heat Addition

We can use the first law for a control volume 


$\dot{E} = \dot{Q} - \dot{W} + \sum_{}\dot{m}h_1 - \sum_{}\dot{m}h_2$

From our assumptions, this becomes:
$$
\dot{Q} = \dot{m}(h_2 - h_1)
$$

Looking at the steam tables we can find that 

$h_1 = 2794.1\ \text{kJ/kg}$

$h_2 = 945.1\ \text{kJ/kg}$


$\dot{Q}_{in} = \dot{m}(h_2 - h_1)$


$\dot{Q}_{in} = 28{,}390(2794.1 - 945.1)$


$\boxed{\dot{Q}_{in} = 52.5\ \text{MW}}$

## Turbine Work Output

Boiler Outlet Temperature (Turbine Inlet Tempurature): $T_o = 290\ \text{C}$

From the IAEA document, the standard condenser inlet conditions are listed as the water entering will a quality of: $\{x} = 0.85$
which means that the water leaving the turbine has this quality. The pressure after leaving the turbine is also much lower compared to the turbine inlet and from the sources was given to be $\{P_c} = 5\ \text{kPa}$

Looking at the saturated vapor table at 5kPa and using the equation $\{h_3} = \{h_f}(1-x) + \{h_g}x$ where $h_f = 151.53\ \text{KJ/kgK}$ and $h_g = 2567.4\ \text{KJ/kgK}$, we can find the the value for $h_3$

$\begin{aligned}
h_3 &= {h_f} (1-x) + x {h}_{fg} \\
    &= 151.53 (1-0.85) + 0.85(2567.4) \\
    &= 2205.02\ \text{kJ/kg}
\end{aligned}$

From the First Law for a CV: 

$\dot{W}_{out} = \dot{m}(h_2 - h_3)$

$\dot{W}_{out} = 28{,}390(2794.1 - 2205.02)$

$\boxed{\dot{W}_{out} = 16.7\ \text{MW}}$

## Thermal Efficiency

To find the thermal efficiency of the plant, we can use the equation 

$\eta_{th} = \frac{\dot{W}_{net}}{\dot{Q}_{in}}$

Because the Back Work Ratio of a Boiling Water Reactor (not using acronyms to avoid confusion) ranges from 0.005 - 0.02, this means the 

${|{W}_{out}|} >> {|{W}_{in}|}$ 

and we can assume it is negligible when computing the overall efficiency of the plant. Now the efficiency equation becomes: 

$\eta_{th} = \frac{\dot{W}_{out}}{\dot{Q}_{in}}$


$\eta_{th} = \frac{16.7}{52.5}$

$\boxed{\eta_{th} = 0.318 \approx 31.8\%}$

---







## Turbine Exit Conditions (State 2)

$$
P_2 = 5\ \text{kPa}
$$

$$
T_2 = 30^\circ\text{C} = 313\ \text{K}
$$

Quality:

$$
x = 0.85
$$

From saturated steam tables:

$$
h_f = 151.53\ \text{kJ/kg}
$$

$$
h_{fg} = 2567.4\ \text{kJ/kg}
$$

Exit enthalpy:

$$
\begin{aligned}
h_2 &= h_f + x h_{fg} \\
    &= 151.53 + 0.85(2567.4) \\
    &= 2205.02\ \text{kJ/kg}
\end{aligned}
$$

---

## Turbine Work Output

$$
\dot{W}_{out} = \dot{m}(h_1 - h_2)
$$

$$
\dot{W}_{out} = 28{,}390(2794.1 - 2205.02)
$$

$$
\boxed{\dot{W}_{out} = 16.7\ \text{MW}}
$$

---

## Pump Work

$$
\dot{W}_p \approx 0
$$

---

## Thermal Efficiency

$$
\eta_{plant} = \frac{\dot{W}_{out}}{\dot{Q}_{in}}
$$

$$
\eta_{plant} = \frac{16.7}{52.5}
$$

$$
\boxed{\eta_{plant} = 0.318 \approx 31.8\%}
$$

---

## Summary of Results

| Quantity | Value |
|--------|-------|
| Mass flow rate | 28,390 kg/s |
| Boiler heat input | 52.5 MW |
| Turbine work output | 16.7 MW |
| Plant efficiency | 31.8% |


aaaa