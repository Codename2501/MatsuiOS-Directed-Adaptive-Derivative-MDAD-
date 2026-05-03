# Chapter 4 — Discrete MDAD (Numerical Differentiation)

## 4.1 Basic Discrete Form
In numerical computation, the limit is replaced by a finite OS-generated step:

$$
D_{\text{MDAD}}^{\text{disc}} f(x) = \frac{ f(x + \ell_{\text{OS}}(x)\,\vec d_{\text{OS}}(x)) - f(x) }{ \ell_{\text{OS}}(x) }
$$

The difference formula is simple, but the step itself is OS-generated.

## 4.2 Complex-Step Discrete Form
For singularity avoidance:

$$
D_{\text{MDAD}}^{\text{disc}} f(x) = \frac{ f(x + i\,\ell_{\text{OS}}(x)\,\vec d_{\text{OS}}(x)) - f(x) }{ i\,\ell_{\text{OS}}(x) }
$$

This inherits the numerical stability of complex-step differentiation.
