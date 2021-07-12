Electrical Grids - Glossary
===============

**Active (real) Power**: Power transferred to the load, e.g. the component of the AC current in which the voltage and (positive) current are in phase.

**Reactive Power**: The component of the power in which the voltage and current are $90^\circ$ out of phase, e.g. caused by inductive or capacitive features in the circuit. Common unit is `VAr` or `MVAr` (mega-volt-ampere reactive)

**Complex Power**: The vector sum of the active and reactive power components, represented in the complex plane. The reactive power is represented as purely complex; the active power is real:

$$ S = VI^* $$

**Apparent Power**: The magnitude of the complex power, $|S|$.

**Power factor**: The ratio of real (active) power and the apparent (total complex) power, ranging from $-1$ (completely reactive) to $+1$ (completely active).

**Total harmonic distortion**: The ratio of the square of the higher harmonics to the fundamental harmonic, e.g.:

$$\text{THD} = \frac{\sum_{i=1}^N I_i^2}{I_0}$$

**Inductors**: These components are governed by the following differential equation:

$$\mathcal{E} = -L\frac{dI}{dt}$$

**Capacitors**:

$$ I = C\frac{dV}{dt}$$

**Overcurrent**: A situation with excess current in the circuit, often resulting in excess heat generation or equipment damage. Causes: short circuit; excessive load; design issues; arc faults; ground faults. Solutions include circuit breakers and fuses, as well as current limiters.

**Single-phase electrical power**: A circuit or distribution system in which a single alternating current is present, typical of the 50-60 Hz currents in residential applications (heating and lighting). Main disadvantages:
 - a single-phase motor does not produce a rotating magnetic field; instead, it requires additional circuits to start.

**Two-phase electrical power**: Consists of two wires, with current out of phase by 1/4 cycle. Advantages/disadvantages:
 - The power delivered is constant.
 - Two-phase electrical power is provided by a four-wire circuit.
 - In principle the power is constant, however two-phase power is susceptible to pulsations in power, which can cause e.g. mechanical stress in motors.

**Three-phase electrical power**: Consists of three transmission wires, each carrying an alternating current with an period offset of 1/3. It has several benefits compared to two-phase electrical power:
 - The 
 - A fourth neutral (return) conductor therefore carries very little or no current, and thus can have a much smaller gauge.
 - Summing all three components, the power delivered is constant.

**Shannon Entropy**: A measure of entropy as formulated in information theory.

**Inverter interfaced distributed generators**:

**Relationship between frequency and load**: 

**Tellegen's Theorem**:

**Congestion Management**: ??

Grid Elements
---------

**Shunt**: A shunt reactor absorbs reactive power, and therefore increases the efficiency of a grid.


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
