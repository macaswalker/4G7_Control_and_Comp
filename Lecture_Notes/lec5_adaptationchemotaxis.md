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




## Adaptation Exhibits Integral Action

