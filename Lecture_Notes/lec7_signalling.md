# Signalling in Large Cells

## Directed Swimming in Large, Single Celled Organisms

We have seen previoulsy, when discussing Chemotaxis, that small unicellular organisms can move systematically to find nutrients and avoid danger.

Other unicellular organisms also achieve this, and are capable of sensing, acting and mocing on a faster timescale.

## Problem: Diffusion Limits the Speed of Intracellular Signals

Intracellular signaling in small cells typically relies on diffusion to transmit signals over distance - how long does this take:

- Diffusion: $ \mathbb{E} (|\mathbf{x}(t)|^2) = 2nDt$

Different organisms have different characteristic length scales, which are the typical size a molecule needs to travel to deliver a signal inside the cell.

What effect does a delay have on an uncertain closed feedback loop system?

## Ion Pumps, Ion Gradients and Ion Channels

Cells transprt ions across **lipid bilayer membranes** for **osmotic balance** and **pH balance**. 

They move through **ion channels**:

When a membrane is **selectively permeable** to an ion and there is a **concentration gradient** across it, a **voltage** develops, described the the **Nernst equation**:

$$
E_{\text{Nersnt}} = \frac{RT}{zF} ln \frac{c_{out}}{c_{in}}
$$

Many cells have a **nonzero retsing membrane potential**, ususally **negative inside** relative to outside.

## Electrical Compartmental Model of Cells


Cells can be modeled electrically by assuming fixed ion concentrations across the membrane and modeling the membrane’s **capacitance** and **ion channel conductances**.
- The core equation for membrane voltage dynamics is:

$$
c_m \frac{dV}{dt} = \sum_i g_i (E_i - V)
$$

where:
- $c_m$ = membrane capacitance,
- $g_i$ = conductance of ion channel $i$,
- $E_i$ = equilibrium (Nernst) potential for ion $i$.

- **Ion channel conductances** $g_i$ are **dynamic** — they change with voltage, temperature, pH, mechanical stress, and other biochemical signals.
- **Membrane conductance** is usually nonzero, so the **membrane time constant** (how fast voltage changes) is **small** (around 1–10 ms).

## Ion Channels have Multiple, Discrete Internal States

It is possible to measure currents of indivudual ion channels.

The channel currents appears as discrete evets - brief openings taht conform to a discrete state random process.

The dwell times in these states are often exponentially distributed, indicating a **memoryless process** (Markovian)

The plotting of these dwell times shows that the system is memoryless as it follows an exponential curve, hence the porbability seems to remian constant.

E.g.:

$$
P(\text{still open at time } t) = e^{- \lambda t}
$$

Hence, $\lambda$ stays constant.

## Membrane Excitability & Voltage Gated Channels

Many ion channels are **voltage-gated** - they are open or closed depending on the membrane potential (the voltage across the cell membrane)

The size and the charge of the pore helps determine which ions can pass through.

## Fast vs Slow IV Characteristics: The Essence of Excitability

Long before ion channels were identified, Hodgkin & Huxley studied voltage-gated conductance in the squid giant axon!

By **voltage clamping** (fixing the membrane potentials at different values) and measuring the resulting ionic currents, they were able to isolate the $K^+$ and $Na^+$ components of the membrane current.

They also measured the IV properties at fast and slow timescales, revealing a strong instability at fast timescales.

The IV curve is the current vs-voltage relationship:

1. Fast I-V Characteristics: nonlinear unstable behaviour, small chnages can cause a huge spike in current
2. Slow I-V Characteristics: slower timescales, behaviour is more stable and more linear

## The Hodgkin-Juxley Model

Inspired by a kinetic model, HH built an empirical model of the membrane conductances underlying the action potnetial in the giant axon.

$$
C \dot{V} = I - g_L (V - E_L) - g_K n^4 (V - E_K) - g_{\text{Na}} m^3 h (V - E_{\text{Na}})
$$

$$
\tau_m(V) \dot{m} = m_\infty(V) - m
$$

$$
\tau_n(V) \dot{n} = n_\infty(V) - n
$$

$$
\tau_h(V) \dot{h} = h_\infty(V) - h
$$

Ion channels are present in **all known cellular life forms**. 


---

# Assigned Reading

1. Unique features of action potential initiation
in cortical neurons

2. Hodgkin and Huxley model—still standing?.