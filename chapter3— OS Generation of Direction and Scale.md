# Chapter 3 — OS Generation of Direction and Scale

## 3.1 Scale Generation
OS Geometry generates a hierarchical scale:

$$
\ell_{\text{OS}}(x) = \ell_0 \, 2^{k(x)}
$$

where $k(x) \in \mathbb{Z}$ is chosen by the OS based on M/E/S evaluation.

- Unsafe region → larger scale  
- Safe region → smaller scale  

## 3.2 Direction Generation
OS-dir generates the direction:

$$
\vec d_{\text{OS}}(x) = \arg\min_{\vec d \in \mathcal{D}} M(x,\vec d)
$$

where:

- $\mathcal{D}$ is a finite set of candidate directions
- $M(x, d)$ measures local concentration or instability

## 3.3 Mode Selection
The OS chooses:

- Real direction (normal mode)
- Complex direction (singularity avoidance)
