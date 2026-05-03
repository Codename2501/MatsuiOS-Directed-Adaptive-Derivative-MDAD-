# Chapter 2 — Continuous Definition of MDAD

## 2.1 OS-Generated Quantities

For a point $x$, MatsuiOS generates:

* **Direction vector**: $\vec d_{\text{OS}}(x) \in \mathbb{C}^n$
* **Scale**: $\ell_{\text{OS}}(x) > 0$
* **Mode**: $\text{mode}_{\text{OS}}(x) \in \{\text{real}, \text{complex}\}$

These depend on internal OS logic such as $M/E/S$ evaluation and singularity detection.

## 2.2 Continuous MDAD Definition

For a function $f: \mathbb{C}^n \to \mathbb{C}$, the MDAD is defined as:

$$
D_{\text{MDAD}} f(x) = \lim_{\varepsilon \to 0} \frac{ f\!\left(x + \varepsilon \, \ell_{\text{OS}}(x) \, \vec d_{\text{OS}}(x)\right) - f(x) }{ \varepsilon \, \ell_{\text{OS}}(x) }
$$

The key difference from classical derivatives is that both the direction and the scale are *generated* by the OS.

## 2.3 Singularity Avoidance via Complex Step

When a singularity is detected, the OS switches to complex-step mode:

$$
D_{\text{MDAD}} f(x) = \lim_{\varepsilon \to 0} \frac{ f\!\left(x + i \, \varepsilon \, \ell_{\text{OS}}(x) \, \vec d_{\text{OS}}(x)\right) - f(x) }{ i \, \varepsilon \, \ell_{\text{OS}}(x) }
$$

This provides exceptional numerical stability.
