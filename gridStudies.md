Electrical Grids - Glossary
===============

**Active (real) Power**: Power transferred to the load, e.g. the component of the AC current in which the voltage and (positive) current are in phase.

**Reactive Power**: The component of the power in which the voltage and current are $90^\circ$ out of phase, e.g. caused by inductive or capacitive features in the circuit. Common unit is `VAr` or `MVAr` (mega-volt-ampere reactive). Certain loads *require* reactive power, and therefore a technique called **reactive compensation** is used to provide that required reactive power, using e.g. a **shunt capacitor**.


**Consuming and producing reactive power**: The convention is that inductors are said to "consume" reactive power, and capacitors are said to "generate" reactive power.

**Complex Power**: The vector sum of the active and reactive power components, represented in the complex plane. The reactive power is represented as purely complex; the active power is real:

$$ S = VI^* $$

**Apparent Power**: The magnitude of the complex power, $|S|$.

**Power factor**: The ratio of real (active) power and the apparent (total complex) power, ranging from $-1$ (completely reactive) to $+1$ (completely active). Also sometimes referred to as the $\bf{\cos(\phi)}$.

**Total harmonic distortion**: The ratio of the square of the higher harmonics to the fundamental harmonic, e.g.:

$$\text{THD} = \frac{\sum_{i=1}^N I_i^2}{I_0}$$

**Inductors**: These components "consume" reactive power, and are governed by the following differential equation:

$$\mathcal{E} = -L\frac{dI}{dt}$$

**Capacitors**: These "generate" reactive power:

$$ I = C\frac{dV}{dt}$$

**Inverters (Inverter) and Rectifiers (Gleichrichter)**: Inverters convert DC power to AC power; rectifiers convert AC power to DC power.

**static VAR compensator (SVC)**: "a set of electrical devices for providing fast-acting reactive power on high-voltage electricity transmission networks."

**Series capacitors**:

**Synchronous condensors**:

**Shunt Admittance**: 

**R/X-ratio**: 

-----------
Impedance-Admittance, Resistance-Conductance, Reactance-Susceptance
----------
**Impedance, Resistance (real), and Reactance (imaginary)**: $Z = R + jX$

**Admittance ($Y$)**: The (complex) reciprocal of impedance, e.g. $Y\equiv\frac{1}{Z}$.

**Conductance ($G$)**: The reciprocal of resistance, e.g. $G=\frac{1}{R}$

**Susceptance ($S$)**: The reciprocal of reactance, e.g. $B=\textrm{Im}(Y)$.

-----------
**Overcurrent**: A situation with excess current in the circuit, often resulting in excess heat generation or equipment damage. Causes: short circuit; excessive load; design issues; arc faults; ground faults. Solutions include circuit breakers and fuses, as well as current limiters.

**Single-phase electrical power**: A circuit or distribution system in which a single alternating current is present, typical of the 50-60 Hz currents in residential applications (heating and lighting). Main disadvantages:
 - a single-phase motor does not produce a rotating magnetic field; instead, it requires additional circuits to start.

**Two-phase electrical power**: Consists of two wires, with current out of phase by 1/4 cycle. Advantages/disadvantages:
 - The power delivered is constant.
 - Two-phase electrical power is provided by a four-wire circuit.
 - In principle the power is constant, however two-phase power is susceptible to pulsations in power, which can cause e.g. mechanical stress in motors.

**Three-phase electrical power**: Consists of three transmission wires, each carrying an alternating current with an period offset of 1/3. It has several benefits compared to two-phase electrical power:
 - A fourth neutral (return) conductor therefore carries very little or no current, and thus can have a much smaller gauge.
 - Summing all three components, the power delivered is constant.

In Europe, a 400V (RMS) three-phase system, the voltage between any two lines (the **line voltage**) is 400V. This is a factor of $\sqrt{3}$ larger than the voltage between any one line and neutral. To reach the $230V=\frac{400V}{\sqrt{3}}$ voltage level coming out of the wall socket, one "live/active/hot" line and the neutral line are used (and possibly a ground line).

**Shannon Entropy**: A measure of entropy as formulated in information theory.

**Sensitivity Matrix**: Something to do with the Reactive power sensitivity ($dV/dQ$)... and an ?

**Inverter interfaced distributed generators**:

**Relationship between frequency and load**: 

**Tellegen's Theorem**:

**Karush–Kuhn–Tucker conditions**:

**Congestion Management**: ??

--------
**Power flow vs Optimal power flow**: The power flow can be numerically solved for e.g. the voltage, voltage phase angle, and the real and reactive power flowing through each line. The Optimal power flow is one such calculation that also determines the minimal cost per kilowatt, presumably assuming that the generator outputs are degress of freedom that can be modified.

**Slack bus**: This is the bus, generally a generator bus, that is used to balance the active and reactive power (i.e. absorbing reactive power from the transmission lines and other elements) in the system. It defines the system's reference phase angle.

**State Estimation**: Given measurements of the bus voltages, bus $p$ and $q$, and line $p$, with their uncertainties, use a least squares estimator to better constrain the system and therefore reduce the uncertainties of said measurements.

**Unit commitment**: This refers to the [day-ahead] planning process of determining which generators (and/or subunits) to commit to generation for the upcoming e.g. days. This is particularly important for generators that have a longer warm-up time. Also, in a free-market system, it may not be possible to instruct certain units to shut off completely (?).

**Distribution Grid**: This is the medium-range grid that lowers the transmission line voltage down to 2-35 kV level, where it is then distributed to e.g. a residential area, and finally stepped down to "operational usage" (220V).

**Short circuit calculation**: A calculation of the minimum or maximum short-circuit currents in a network. 

-----------
Grid Elements
---------

**Motor**: A motor has a 

**Shunt**: A shunt reactor absorbs reactive power, and therefore increases the efficiency of a grid.

**Ward Equivalent**: "a combination of a constant apparent power consumption and a constant impedance load". In general however, the Ward Equivalent is a generalization of the Thévenin equivalent, in order to replace a potentially complex system with a smaller (often simplified) equivalent to simplify a calculation.

**Induction motor**: This type of motor creates a magnetic field in the stator, which *then produces a magnetic field in the rotor*, and then the relative offest between the stator and the rotor causes the rotor to *spontaneously* start rotating. The rotor will always rotate slightly slower than the stator magnetic field, therefore causing a *slip* of 1-5%. For a good visualization see [this youtube video](https://www.youtube.com/watch?v=AQqyGNOP_3o).

**Induction generator**: An asynchronous generator that uses the principle of an induction motor to *generate* power.

**thyristor-controlled reactor**:

**thyristor-switched capacitor**:

**saturated reactor**:

**high-power ac thyristor controller**:

**series capacitor**:

**synchronous condenser**:

**tap changer controllers**: For a transformer... ?

**droop controllers**: E.g. in PV plants, this adapts the reactive power depending on the bus voltage. ??

**three-winding transformer**: 


Some basic questions that have come up:
---------
**How to increase power in a synchronous generator**: Obviously you cannot change the frequency, which is fixed to the grid. If your generator functions using electromagnets (as opposed to permanent magnets), you can increase or decrease the magnetic field simply by changing the current in these electromagnets. Otherwise there is something like the torque angle...?


Symmetrical Components Method
---------
This is a technique for studying three-phase power systems, by representing (possibly asymmetric) "phasors" (phase vectors representing sine functions in the complex plane) as a linear combination of symmetric phasors in the complex plane. The symmetrical components are referred to as "direct" (positive), "inverse" (negative), and zero (homopolar).

Consider a three-phase circuit transmitted by wires ABC, in which the peaks of the dominant amplitude arrives in that order (ABC), each with a 120$^\circ$ phase offset, and call this the direct or positive component. Then the **negative sequence current** refers to the component whose phases are oriented in the inverse direction (CBA). Finally, a third configuration exists, one in which all three phases are aligned (**Zero sequence current**) If there is no return line, then a zero sequence current cannot exist. Any *balanced* three-phase circuit can be described using a linear combination of these three components.

**Sequence filters** can be used to detect negative or zero sequence current, and form the basis of relays to detect faults and e.g. trip circuit breakers.

HV Current
======

HVDC vs HVAC: Advantages and Disadvantages
 - See https://en.wikipedia.org/wiki/High-voltage_direct_current

-----------------
Fault Detection and Clearing
------------

An **electrical fault** refers to any "abnormal" electrical current -- a short circuit, or a ground fault, etc. **Fault clearing** refers to the restoration of nominal electrical conditions to the circuit.

**Transient faults** (bird contact; lightning strike; temporary tree contact) can be cleared simply by "turning the circuit on and off again." **Persistent faults** include mechanical damage to an underground power cable.

Fault detection in Transmission lines
----------
In (three-phase?) transmission lines, electrical faults can be classified as *asymmetric* or *symmetric*. Asymmetric faults come in flavors:
 - (L-L) Line-to-line: a short-circuit between two lines (5-10%)
 - (L-G) Line-to-ground (65-70%)
 - (double L-G) Double line-to-ground: two lines come in contact with the ground (and each other? <- necessary condition??) )(15-20%)
 - (L-L-L) or (L-L-L-G) line-to-line-to-line (-to-ground) (2-5%). The system remains balanced (what are the implications?), but severe damage is possible.

Problems in Network Operation
==========

**Reactive power management** (in a distribution grid): 

**Voltage control/stabilization**: 

**State Estimation**: 

**Short-circuit calculation**:


**Optimal Transmission Switching**: The process of switching transmission line busses to solve problems of congestion, respect transmission current limits, thus avoiding expensive redispatching.

**Related: N-1 Contingency**: 

Working with Network Code
========

NetworkX
---------
A framework for representing graphs that is used by both network researchers and machine learning experts.

PandaPower
---------
A framework for calculating optimal power system modeling and power flow optimization. **Developed (partially?) at IEE**.

Grid2Op
---------
A framework for training reinforcement learning algorithms for e.g. fault prevention and redispatching, using PandaPower as a backend.

---------------------
Open Areas of Study in Smart Grids
==============

<span style="color:blue">Fault Detection in Microgrids</span>
---------
The distributed and small-scale nature of microgrids make **microgrid fault detection** more difficult. Typical techniques that rely on overcurrent detection or negative sequence current are not able to pick up microgrid faults. The new techniques under development use wavelet transforms or fourier transforms to extract features, which are then fed into classifier tools (e.g. decision trees) for binary classification.

**Unintentional islanding events**, in which distributed generators are isolated from the main grid, pose safety concerns for utility workers, and prevent automatic re-connection of devices (??). Techniques to identify these events include sliding window optimization, SVMs and ANNs.

<span style="color:blue;font-style:italic">
Interestingly, the Wikipedia page on islanding detection in microgrids argues that the problem is over-studied, and that the condition in which a microgrid would continue to operate (the so-called *balanced condition* in which the load and generation is exactly balanced) is anyway very remote, and even the most rudimentary protections will generally catch a typical islanding event.
</span>

**Natural language processing** has been used to identify outages using twitter and other social network feeds.

Features in the Data
===========
 - ROCOF (Rate of change of frequency): Used in microgrid islanding detection.
 - Active and reactive power, and power factor:


--------------
Papers
=============

The following is a rewiew of some papers in the literature:

Power Networks
--------

[Quadratic programming-based grid optimization algorithms for real-time applications](https://ieeexplore.ieee.org/document/8571652) (Martin Braun, Sebastian Wende -- von Berg).
This paper concerns a **reactive power optimizer**, and considers three methods to speed up its computation: (1) selective updating of sensitivity matrices; linear approx. of power flows; extracting sensitivity matrices from the power flow solver. The focus is on **reactive power of distributed generators (DGs)**. It grew out of **SysDL 2.0** and **OpSimEval** sub-projects. Tests are: minimize reactive power at the slack generator, or minimize grid losses.

Testing Automated Operation and Control Algorithms for Distribution Grids Using a Co-simulation Environment (Martin Braun et al). This paper...

Market Considerations
--------
[Cost- or market-based? Future redispatch procurement in Germany](https://www.bmwi.de/Redaktion/EN/Publikationen/Studien/future-redispatch-procurement-in-germany.pdf?__blob=publicationFile&v=2) The main issue that this report points out is that a "last-minute" market will be subject to perverse incentives (so-called "inc-dec" strategies). Generators in regions of **scarcity** will lower their price in order to “price themselves into the market,” knowing that they can “buy back” their energy (e.g. not produce the energy) at a higher price. Generators in regions of **abundance** will raise their price to withhold their energy, knowing that they will be able to sell their energy at a higher cost in the redispatch market. The final report of the project "Beschaffung von Redispatch" commissioned by the German Federal Ministry for Economic Affairs and Energy (Project No. 055/17) (October 2019) recommends against a last-minute market, in favor of a few other proposed measures.

[Design and evaluation of a last-minute electricity market considering local grid limitations](https://ieeexplore.ieee.org/document/9221870). Mike Vogt et al. This paper describes how a "last-minute" market (after the 15-minute market) can be used to resolve schedule deviations from renewable energy sources, which have become quite dramatic with the introduction of more renewable energy sources. The market can be constructed by making a call for bids based on both the schedule deviation forecast and the line capacity forecast. Bidders include batteries, electrolyzers, and combined heat and power (CHP) plants. These sources can either consume or produce energy (also electrolyzers?) to balance the grid, as needed. The costs are paid by the renewable source, e.g. the wind turbine operators. Overall costs of the system can be reduced in this way (also by the system operators, who pay less in balance compensation).

[A co-simulation of flexibility market based congestion management in Northern Germany](https://ieeexplore.ieee.org/document/8916252). Mike Vogt et al. This paper...


Machine Learning on Power Networks
--------

[Learning to run a power network challenge for training topology controllers](https://arxiv.org/abs/1912.04211).
Antoine Marot, Benjamin Donnot et al.
This paper reviewed the winning strategies from the first L2RPN challenge, and compared it to an "oracle" which analytically calculates the perfect response.

[Reinforcement Learning for Electricity Network Operation - A White paper](https://arxiv.org/abs/2003.07339)
Adrian Kelly, Aidan O'Sullivan, Patrick de Mars, Antoine Marot. This is the white paper for the L2RPN challenge.

[Introducing Machine Learning for Power System Operation Support](https://arxiv.org/abs/1709.09527).
Benjamin Donnot, Isabelle Guyon, Marc Schoenauer, Patrick Panciatici, Antoine Marot.
This paper, by the RTE crew, investigates machine learning techniques for the problem of bus reconfigurations and line disconnections for remedial solutions to prevent transmission lines reaching their thermal limits.

[Winning the L2RPN Challenge: Power Grid Management via Semi-Markov Afterstate Actor-Critic](https://openreview.net/pdf?id=LmUJqB1Cz8)
This paper....

[Learning to Solve Network Flow Problems via Neural Decoding](https://arxiv.org/pdf/2002.04091.pdf)
This is the paper that uses neural networks to improve the solve time (by a factor of 10) for linear network flow problems, by leveraging "duality". If I understand it correctly it is very clever -- it uses a neural network to predict the (scalar) solution to the optimal power flow problem, and then (somehow) decodes the gradients of that NN to find the solution. I am not sure how it works, but it is cool.

[Adaptives Netzäquivalent mit Künstlichen Neuronalen Netzen](https://www.tugraz.at/fileadmin/user_upload/tugrazExternal/4778f047-2e50-4e9e-b72d-e5af373f95a4/files/kf/Session_D3/431_KF_Liu.pdf) This article summarizes a method to use ANNs in order to estimate network equivalents, for example to summarize the behavior of a region of the grid (?) in order to e.g. share information between network operators (while e.g. respecting rules about data anonymity). There are mathematical algorithms to solve this problem, but they are slower (or perhaps not possible to run) in the case of e.g. topology changes. The ANN outperforms one of these methods ("REI") quite significantly.


Physical Constraints On Networks
---------

[Linearly Constrained Neural Networks](https://arxiv.org/pdf/2002.01600.pdf)
This paper is very cool. If you can define a linear constraint that the problem $f[\vec{x}] = \vec{y}$ must obey, then you can construct your neural network in such a way that the constraint is obeyed by construction. (Need to see an example of how this is implemented in practice...!)

[Lagrangian Neural Networks](https://arxiv.org/pdf/2003.04630.pdf)
This paper discusses how a "black-box Lagrangian" can be learned by an appropritely constructed neural network. The work extends models that use a Hamiltonian construction, and argues that the Lagrangian formulation is more flexible. It also implements a simple Graph network example: a wave propagating down a one-dimensional string.

Graph Neural Networks
----------

[Relational inductive biases, deep learning, and graph networks](https://arxiv.org/pdf/1806.01261.pdf)
This paper is the companion paper to the graph_nets package, and argues that introducing structure (e.g. graphical structure) to neural networks allows a "best of both worlds" (structured solutions vs e.g. structure-free neural networks) solution, with more efficient solutions.

Norddeutsches Reallabor Grants
-----------

[Teilvorhaben: Modellierung der Wirtschaftsregion Lübeck sowie KI-Verfahren für sektorübergreifende und integrierte Netzplanung, Netzbetrieb und Marktteilnahmen](https://www.enargus.de/pub/bscw.cgi/?op=enargus.eps2&q=%2201225382/1%22&v=10&p=1&id=2012495)

[Teilvorhaben: Projektmanagement, Gesamtsimulation, Datenintegration und -analyse](https://www.enargus.de/pub/bscw.cgi/?op=enargus.eps2&q=%2201225382/1%22&v=10&p=2&id=2011922)


Other
--------

[A Machine Learning Approach to Methane Emissions Mitigation in the Oil and Gas Industry.](https://www.climatechange.ai/papers/neurips2020/20/paper.pdf)
[(Slides)](https://www.climatechange.ai/papers/neurips2020/20/slides.pdf)
This paper seeks to improve the process of detecting and fixing methane gas leaks by
predicting which "super-emitting" sites should be tested first. The problem is treated as
a binary classification problem, in which each site is classified as super-emitter or
non-super-emitter based on a cutoff point determined by the marginal return of surveying
additional sites (which seems a bit arbitrary). Based on this binary classification,
the group tries various classifiers to optimize the problem, finding logistic regression
to be the best-performing. I personally find the binary classification to be a bit
restrictive: it treats a 200 kg CH<sub>4</sub>/day the same as a
2000 kg/day emitter, whereas you would probably want your algorithm to not treat these
equally. Instead, it might make more sense to ask the algorithm to predict the magnitude
of the emissions directly, and prioritize from there. This also would likely have the
advantage that the data in the middle of the distribution is more useful to the ML
algorithm, which probably relies more heavily on the more extreme data to make its
predictions.

-------------
Bibliography
===========
 - Zhang, Huang and Bompard, *Big data analytics in smart grids: a review*. Energy Informatics, April 2018.
 - Brown, Schlachtberger et al, *Synergies of sector coupling and transmission reinforcement in a cost-optimised, highly renewable European energy system*. Energy, 2018.
 - Wiese, Schlecht et al, *Open Power System Data – Frictionless data for electricity system modelling*. Applied Energy, 2019.
