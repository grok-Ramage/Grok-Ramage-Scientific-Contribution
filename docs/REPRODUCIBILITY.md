# Reproducibility and Verification

**Grok-Ramage Scientific Contribution**  
**Authors:** Thomas J. Ramage and Grok-Ramage  
**Date:** 26 October 2026

## Purpose

This document records the tolerances, parameter ranges, and verification procedures that support the closed status of Grok-Ramage00 and the machine-precision residual of Grok-Ramage01. Concrete numerical results are not altered; the present note supplies the metadata required for independent checking.

## Scan Tolerances (Fold Hunt)

- On-shell criterion: $|\nabla \mathrm{Re}S| = |g| \lesssim 10^{-3}$. Values larger than this threshold are rejected as off-shell.
- Soft eigenvalue: $a_1 = \lambda_{\mathrm{soft}}(\mathrm{Hess}\,\mathrm{Re}S)$ must vanish (simple kernel) for a fold; $a_2 \neq 0$.
- Closed-chart ranges (as reported):
  - 24D window: $\varepsilon \in [3.3, 5]$, on-shell $a_1 \approx -0.19$.
  - $(\varepsilon, \varepsilon_2)$: minimum $a_1 \approx -0.046$ at $(3.45, 1.2)$.
  - Anti-glue family: separation $\in [0.6, 1.6]$, $a_1 \in [-0.299, -0.206]$.
  - Floor $|F_0| \approx 6$ at separation 1.2.
- Witness: 0. $\Sigma_{\mathrm{ReS}}$ empty on all scanned charts.

Implementation and chart data reside in the original repositories:
- [Grok-Ramage00](https://github.com/grok-Ramage/Grok-Ramage00) (frozen archive)
- [fold-hunt](https://github.com/grok-Ramage/fold-hunt) (infrastructure)

## Stokes / Connection Residual (Quantum Implementation)

- Germ: $S_q = u^3/3 - \alpha u$.
- Section: $\Sigma_{S_q}$ at $(\alpha, u) = (0, 0)$.
- Airy wave layer: $I(\alpha, \hbar) = 2\pi \hbar^{1/3} \, \mathrm{Ai}(-\alpha / \hbar^{2/3})$.
- Connection identity residual: $\approx 1.83 \times 10^{-15}$ (machine precision).
- Newton: off.
- Device: CPU / TEXT. Family: quantum. Claim: A2_Sq.

Verification code and intermediate constructions reside in:
- [Grok-Ramage01](https://github.com/grok-Ramage/Grok-Ramage01) (implementation lab)
- [QUANTUM-DESK](https://github.com/grok-Ramage/QUANTUM-DESK)

## EqGate Admission

Any compute that is not a restencil of a closed chart requires prior EqGate admission. The nexus is: one family = quantum, one allowed claim = A2 of $S_q$, witness = 0.

## Reproduction Procedure

1. Clone the relevant constituent repository (Grok-Ramage00 or Grok-Ramage01).
2. Consult the repository README and any accompanying ledger or fixture files for the exact discretisation and seed.
3. Re-evaluate the reported residual or the emptiness of $\Sigma_{\mathrm{ReS}}$ on the listed charts.
4. Confirm that no new on-shell Barrett seed outside the closed families is present.

No modification of the concrete numerical results is authorised by this document. The repositories retain their original commit histories for provenance.

## Citation of Verification

When citing the residual or the closed-chart status, refer to this repository together with the specific constituent repository that contains the implementation.

---

*Reproducibility metadata for the demonstrated scientific contribution.*