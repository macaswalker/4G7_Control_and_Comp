# Populations, Couples Oscillators and CPGs

# Cells Communicate

A common way for cells in a population (tissue, colony) to communiate is via **secretion**

It occurs in specialised structures called **synapses**

Depending on the type of ionic current associated with the receptor, the resulting signal can **depolarise** (excite) or **hyperpolarise** (inhibit) the membrane, or modify kinetic properties of the membrane current. 


## Population Coupling and Oscillations

**quorum sensing** - releasing chemial signals into their environment

## Oscillations in the Nervous System: Control of Animal Movement

In animal, coordinated rhythmic movement is controlled by interactions of neurons in motor circuits

- control of voluntary and involuntary movement involves numerous circuits in more complex animals
- many of the basic architectures and dynamics are generic and involve movement that is patterned in tme, with consistent phase relationships between muscle groups
- neurl circuits that recognise these patterns are called **coupled pattern generators** (CPGs)

## CPGs are often formed by coupling intrinsic oscillatory cells

CPGs contain cells that can oscillate in the absence of any input - **pacemaker cells** - they contian a stable limit cycle

These **apcemaker cells** can be modulated by **neuromodulators**, which can be tweaked the ion channel properties.

## How can we understand the behaviour of coupled oscillators?

It is useful to define an oscillator state in terms of a single variable, **phase $\theta$**

If this is possible, as oscillators dynamics can be written as:

$$
\dot \theta = \omega \text{ mod } T
$$

where $\omega$ is the oscillator frequency.

Relating this back to the state variables, $x$ in the original oscillator, we see that:

$$
\dot x = f(x) \\
\rightarrow \dot{\theta} = \nabla_x \theta \cdot \frac{dx}{dt} = \nabla_x \theta \cdot f(x) = \omega
$$

This defines an **isochron** in the original system.

A **PRC** (phase resetting curve) maps the initla phase to a new phase after a perturbation. 

These two things tells us how external influence change the timing of oscillators.

Notice, that for small perturbations to the flow:

$$
\dot \theta = \nabla_x \theta( f(x)+ \epsilon p(t))
$$

which is simply

$$
\dot \theta = w + \epsilon \nabla_x \theta p(t)
$$

If the direction of $p$ is fixed, then the second term is just the phase resetting curve (PRC).

The PRC term can model interactions between oscillators, e.g.a conductance pulse due to synaptic coupling, with another oscillator, resulting in the **Kuramtot model**:

$$
\dot{\theta}_i = \omega_i + \sum_j H_{ij}(\theta_j - \theta_i) \quad \text{mod } 2\pi
$$

For example, suppose we have two oscillators with differing internal frequencies:

$$
\dot \theta_1  = \omega_1 +K_1sin(\theta_1- \theta_2) \\
\dot \theta_2  = \omega_2 +K_2sin(\theta_1- \theta_2) 
$$

Let $\phi = \theta_1- \theta_2$, then:

$$
\dot \phi   = \omega_1 - \omega_2  +(K_1 + K_2) sin(\theta_1- \theta_2) 
$$

If a steady state exists, then there are stable and unstable fixed points given by:

$$
\phi_{\text{fp}}   = \arcsin \frac{\omega_1 - \omega_2}{K_1 + K_2}
$$

## Population Oscillations in Non-Oscillating Components

Suppose we have a population of cells (E) that secrete excitatory neurotransmitter interconnected with a population of inhibitory cells (I):

The interactions  between EI cells can cause oscillations!

Suppose we model the time-averaged firing rates as:

$$
\tau_E \frac{dE_i}{dt} = -E_i + \text{sat}\left(\sum_j w_{ij}^{EE} E_j - \sum_j w_{ij}^{IE} I_j + u_i\right)
$$

$$
\tau_I \frac{dI_k}{dt} = -I_k + \text{sat}\left(\sum_j w_{kj}^{EI} E_j\right)
$$

where:

- $E_i$ = firing rate of excitatory cell $i$
- $I_k$ = firing rate of inhibitory cell $k$
- $\tau_E, \tau_I$ = time constants
- $w^{EE}, w^{IE}, w^{EI}$ = connection strengths
- $u_i$ = external input to E cells
- $\text{sat}(\cdot)$ = saturation function preventing rates from diverging

When we consider under a simplifed form: 

$$
\tau_E \frac{dE}{dt} = -E + \text{sat}(w_{EE} E - w_{IE} I + u)
$$

$$
\tau_I \frac{dI}{dt} = -I + \text{sat}(w_{EI} E)
$$

## Population Oscillations in the Brain

Measurements of brain activity across large populations revlea peaks in the power spectrum at several frequencies in the range $1-80$ Hz. 

We investigate this further in the assigned reading.

---

# Assigned Reading

1. The onset of collective behavior in social
amoebae

2.  Neuronal synchrony: a versatile code for the definition of relations

3. Noise, neural codes and cortical organization




