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

---

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

---

## Turbine Work Output

Boiler Outlet Temperature (Turbine Inlet Tempurature): $T_o = 290\ \text{C}$

From the IAEA document, the standard condenser inlet conditions are listed as the water entering will a quality of: $\{x} = 0.85$
which means that the water leaving the turbine has this quality. The pressure after leaving the turbine is also much lower compared to the turbine inlet and from the sources was given to be $\{P_c} = 5\ \text{kPa}$

Looking at the saturated vapor table at 5kPa and using the equation $\{h_3} = \{h_f}(1-x) + \{h_g}x$ where $h_f = 151.53\ \text{KJ/kg}$ and $h_g = 2567.4\ \text{KJ/kg}$, we can find the the value for $h_3$

$\begin{aligned}
h_3 &= {h_f} (1-x) + x {h}_{g} \\
    &= 151.53 (1-0.85) + 0.85(2567.4) \\
    &= 2205.02\ \text{kJ/kg}
\end{aligned}$

From the First Law for a CV: 

$\dot{W}_{out} = \dot{m}(h_2 - h_3)$

$\dot{W}_{out} = 28{,}390(2794.1 - 2205.02)$

$\boxed{\dot{W}_{out} = 16.7\ \text{MW}}$

---

## Thermal Efficiency

To find the thermal efficiency of the plant, we can use the equation 

$\eta_{th} = \frac{\dot{W}_\text{net}}{\dot{Q}_\text{in}}$

$\eta_{th} = \frac{W_{net}}{Q_{in}}$

Because the Back Work Ratio of a Boiling Water Reactor (not using acronyms to avoid confusion) ranges from 0.005 - 0.02, this means the 

$\abs{x} = 1$

$\{|{W}_{out}|}$ >> $\{|{W}_{in}|}$ 

and we can assume it is negligible when computing the overall efficiency of the plant. Now the efficiency equation becomes: 

$\eta_{th} = \frac{\dot{W}_{out}}\{\dot{Q}_{in}}$


$\eta_{th} = \frac{16.7}{52.5}$

$\boxed{\eta_{th} = 0.318 \approx 31.8\%}$

---

## Turbine Isentropic Efficiency

Now, to find the isentropic efficiency of the turbine, we can use the equation: 

$\eta_{isentropic} = \frac{\dot{W}_{real}}\{\dot{W}_{s}}$

The isentropic effiency measures how much of the work done by the turbine is lost to irreversible processes. To find the isentropic Work, we can set $s_2 = s_3$ which implies that only reversible processes occur in the turbine. Knowning $s_2 = s_3$, we can again look at the saturated water table and compute a new water quality x to then find the associated enthalpy. From the conditions of state 2, $s_2 = s_3 = 5.8529\ \text{KJ/KgK}$

We can find the water quality x from the saturated vapor table at 5kPa $s_f = 0.5210\ \text{KJ/kgK}$ and $s_g = 8.3304\ \text{KJ/kgK}$: 

$\begin{aligned}
s_3 &= {s_f} (1-x) + x {s}_{g} \\
    s_3 = 0.5210 (1-x) + x(8.3304) \\
\end{aligned}$

$x = 0.683$

Now to find $h_{3s}$

$\begin{aligned}
h_{3,s} &= {h_f} (1-x) + x {h}_{g} \\
    &= 151.53 (1-0.683) + 0.683(2567.4) \\
    &= 1801.6\ \text{kJ/kg}
\end{aligned}$

$\dot{W}_{s} = \dot{m}(h_2 - h_{3,s})$
$\dot{W}_{s} = 28{,}390(2794.1 - 1801.6)$
$\dot{W}_{s} = 28.2\ \text{MW}$

$\dot{W}_{real} = 16.7\ \text{MW}$

$\eta_{isentropic} = \frac{16.7}{28.2}$

$\boxed{\eta_{isentropic} = 0.593 \approx 59.3\%}$

## Summary of Results

| Quantity | Value |
|--------|-------|
| Boiler heat input | 52.5 MW |
| Turbine work output | 16.7 MW |
| Plant efficiency | 31.8% |
| Turbine efficiency | 59.3% |


When it comes to the real values of this plant and BWR plants in general the effiency is around 30-34% which confirms the value found using hand calculations. When checking the real value of the power output, the Limerick Power Plant has a much higher posted value, for a single reactor able to produce 1,130MW. The cause of huge discrepency is most likely underestimating the mass flow rate since I was able to find this value for the condenser ONLY and assumed that this was a basic Rankine Cycle in steady state. This means that if there are other devices that increase the efficency of the cycle, say a reheat phase, this means there is more water unaccounted for. When it comes to the turbine efficiency, this was a slight underestimate, usually the isentropic effiencies of turbines in BWRs can range from 80-90%. When looking further into this, BWRs usually use a mix of high pressure and low pressure turbines which are optimized to extract energy from the water at differnet pressures as the water travels through the system after heat is added. This most likely is the biggest reason my efficiency is much lower compared to the real turbine efficiences. 