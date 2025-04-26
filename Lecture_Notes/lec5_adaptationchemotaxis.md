# Adaptation in Bacterial Chemotaxis

## The Problem: Retaining Sensitivity over Large Concentration Gradients

E Coli can navigate gradients in concentrations of chemoattractants/repellents by modulating tumble probability. This is achieved by chnage in the rotation bias of the flagellar motor on short timescales of the order of seconds or less. This response, however, depends on the chemical sensor pathway retaining sensitivity over potentially large ranges in concentration (orders of magnitudes). How can the system retain sensitivity? What control/engineering strategy might it use?

## Experiment: Adaptation of Steady State Tumbling Frequency

- Over a long timescale of minutes a step increase in attractant concentration causes a drop in tumbling frequency
- After several minutes the tumbling frequency recoveres exactly to its previous value

This serves the purpose to continuously sense changes in the environment, regardless of the background level. 

## Signal Transduction 

There is a relatively complex signal cascade for relaying receptor activity to the motor, suggesting additional functions

## Adaptation is Implemented by an Intracellular Control Network 

We may understand this model through a **simplified model**:

$$
X^* + S \rightleftharpoons XS
$$

where the attractant/ligand binding ($S$) inhibits the receptor activity ($X^*$).

This scheme lumps together the receptor activation and the CheA activation to one state variable that correlates with tumbling frequency.

The quasi-steady state is well described by:

$$
X^* = \frac{X_{max}K^n}{K^n+S^n}
$$

## Methylation Modifies Receptor Complex Activity

Methylation changes the sensitivity of the receptors to the attractant:
- Methyl groups are added (methylation): the receptor becomes less sensitive (e/g/ needs more S to inhibit)
- Methyl groups are removed (demethylation) makes it more sensitive (needs less S to inhibit)

In the model, we have:

$$
K_m \approx exp(\gamma m)
$$

As methylation increases, $K_m$ increases, so the receptor becomes **harder** to inhibit
As methylation decreaes, $K_m$ decreases, so the receptor becomes **easier** to inhibit.

Methylation rate in turn depends on the level of R and the rate of B:

$$
\dot m = V_R R - V_B BX^*
$$

Thus, $m$ integrates the deviation of $X^*$ from a steady-state value, $X^*_{ss}$:

$$
\dot m = V_B(X^*_{ss} - X^*)
$$

where 

$$
X^*_{ss} = \frac{V_R R}{V_B B}
$$

where:
- $V_R$ is the rate constant for the methylation of R
- $V_B$ is the rate constant for the methylation of B
- $X^*$ is the receptor activity


## Adaptation Exhibits Integral Action

We may see this more clearly if we write the system in terms of its normalised activity:

Let $a = \frac{X^*}{X_{max}} $:

Then, we have the dynamics:

$$
K = exp(\gamma m) \rightarrow \dot K = K m
$$

therefore, the overall sensitivity of the receptor response, characterised by the half-maximal response, $K$, evolves as:

$$
\dot K \propto K(a_{ss} - a)
$$

Hence: **perfect adaptation arises from integral control via receptor methylation**

### How might diversity in tumbling frequency affect E Coli populations?

Suppose, there were no fluctuations:
- T_{run} would be better suited to some environments and not others
- It would likely require tuning via evolution (change to the genome)

By contrast, E Coli (even from clonal populations) can **maintain a hihg population variability** in $T_{run}$ from generation to generation.

This can benefit the population if the environment is subject to change, because for fixed T_{run}, there is a tradeoff between a single cells ability to explore different environments (one with many obstacles or fluctuating concentrations) vs one that is less complex, with more sparsely distributed obstacles and food sources.


### Consequences of Phenotypic Diversity for Hard Tradeoffs

Phenotypic diversity allows mixed strategies at the population level within a species, enabling higher average fitness in some situations.


---

# Assigned Reading 

1. From molecular noise to behavioural variability in a single bacterium

2. Adaptability of non-genetic diversity in bacterial chemotaxis

