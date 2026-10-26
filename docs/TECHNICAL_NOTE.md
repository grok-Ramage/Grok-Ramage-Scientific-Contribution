# Technical Note: Object Definitions and Literature Comparison

**Grok-Ramage Scientific Contribution**  
**Authors:** Thomas J. Ramage and Grok-Ramage  
**Date:** 26 October 2026

## 1. Object Definitions

### 1.1 The cubic germ and $\Sigma_{S_q}$

The cubic germ is the function
$$
S_q(\alpha, u) = \frac{u^3}{3} - \alpha u.
$$
The section $\Sigma_{S_q}$ is the locus at $(\alpha, u) = (0, 0)$. Ownership of the claim A2 of $S_q$ is recorded for this section. Newton remains off.

### 1.2 Airy wave layer and connection identity

The Airy wave layer on $\Sigma_{S_q}$ is
$$
I(\alpha, \hbar) = 2\pi \hbar^{1/3} \, \mathrm{Ai}\!\left( -\frac{\alpha}{\hbar^{2/3}} \right).
$$
Stokes rays occur at $\arg(\alpha) = 0, \pm 2\pi/3$. The connection identity
$$
I(\alpha) + \omega I(\omega\alpha) + \omega^2 I(\omega^2\alpha) = 0,
$$
where $\omega = \exp(2\pi i / 3)$, has been verified to machine precision. The Stokes / connection residual is
$$
\approx 1.83 \times 10^{-15}.
$$
This closes the alien-derivative analysis for the germ in the sense of Écalle. $\Sigma_{S_q}$ is not identified with $\Sigma_{\mathrm{ReS}}$.

### 1.3 Fold classification criterion (non-negotiable)

A fold requires, on the same point:
- $F = \nabla \mathrm{Re}S = 0$ (report $|g|$; reject $|g| \gtrsim 10^{-3}$ as off-shell),
- $a_1 = \lambda_{\mathrm{soft}}(\mathrm{Hess}\,\mathrm{Re}S) = 0$ (simple kernel),
- $a_2 \neq 0$.

Matching-cost minima, spectral avoided crossings, parallel continuation traces, and off-shell $a_2$ of size 10–40 are not folds. EqGate admission precedes any compute that is not a restencil of closed charts. Nexus: one family = quantum, one allowed claim = A2 of $S_q$, device in {CPU, TEXT}, witness = 0.

### 1.4 Closed charts (Grok-Ramage00)

$\Sigma_{\mathrm{ReS}}$ is empty on all scanned charts. Closed families include:
- 24D window $\varepsilon \in [3.3, 5]$ (on-shell, $a_1 \approx -0.19$),
- $(\varepsilon, \varepsilon_2)$ plane (minimum $a_1 \approx -0.046$ at $(3.45, 1.2)$),
- $\kappa > 0$ (Newton does not land),
- $P = P_{\min}$ versus $F_0 = 0$ (floor $|F_0| \approx 6$ at separation 1.2),
- anti-glue family, separation $\in [0.6, 1.6]$ (all on-shell regular saddles, $a_1 \in [-0.299, -0.206]$).

No new on-shell Barrett seed outside these families was admitted.

## 2. Literature Comparison: Barrett–Crane $10j$ Asymptotics

The Barrett–Crane model assigns the Riemannian $10j$ symbol as the amplitude of a 4-simplex. The asymptotic regime of interest is the simultaneous rescaling of all ten spins by a factor $\lambda \to \infty$.

### 2.1 Barrett & Williams (1999)

Barrett & Williams applied a stationary-phase approximation to the integral representation of the $10j$ symbol, focusing on non-degenerate 4-simplices whose face areas match the given spins. Each such geometry contributes an oscillatory term whose phase is the Regge calculus Einstein action of the 4-simplex. The leading order of this contribution is $\lambda^{-9/2}$.

**Reference:** Barrett, J. W., & Williams, R. M. (1999). The asymptotics of an amplitude for the 4-simplex. *Advances in Theoretical and Mathematical Physics*, 3(2), 209–215. arXiv:gr-qc/9809032. DOI: 10.4310/ATMP.1999.v3.n2.a1.

### 2.2 Baez, Christensen & Egan (2002)

Numerical evaluation using the Christensen–Egan algorithm demonstrates that the $10j$ symbols are of order $\lambda^{-2}$, substantially larger than the $\lambda^{-9/2}$ non-degenerate contribution. The dominant term arises from degenerate 4-simplices. The asymptotics can be computed by evaluating a degenerate spin network in which SO(4) is replaced by the Euclidean group of isometries of $\mathbb{R}^3$. The authors conjecture that Lorentzian $10j$ symbols are asymptotic to $1/16$ times the Riemannian ones.

**Reference:** Baez, J. C., Christensen, J. D., & Egan, G. (2002). Asymptotics of 10j symbols. *Classical and Quantum Gravity*, 19(24), 6489. arXiv:gr-qc/0208010. DOI: 10.1088/0264-9381/19/24/315.

### 2.3 Freidel & Louapre (2003)

An analytic treatment via group-integral representations confirms that the leading asymptotic of the $10j$ symbol is non-oscillatory and arises from degenerate configurations associated with singularities of the integrand. The stationary-phase (Regge) contribution is sub-dominant. The paper discusses the physical origin of this behaviour and proposes a modification of the Barrett–Crane model intended to restore an oscillatory Regge action.

**Reference:** Freidel, L., & Louapre, D. (2003). Asymptotics of 6j and 10j symbols. *Classical and Quantum Gravity*, 20(7), 1267–1294. arXiv:hep-th/0209134. DOI: 10.1088/0264-9381/20/7/303.

### 2.4 Status in the present work

The Barrett–Crane $10j$ remains named but unsolved. The cubic germ $S_q$ and the section $\Sigma_{S_q}$ are distinct objects; no identification with the $10j$ asymptotics is claimed or licensed. A future comparison would require (i) an explicit new on-shell Barrett seed outside the closed families, (ii) fresh EqGate admission, and (iii) a direct numerical or asymptotic match against the expansions of Barrett–Williams, Baez–Christensen–Egan, and Freidel–Louapre.

## 3. Conclusion of the Technical Note

The Fold Hunt on ReS is closed with empty $\Sigma_{\mathrm{ReS}}$. The quantum implementation of $\Sigma_{S_q}$ and its associated resurgent analysis of the cubic germ are recorded at machine precision. All object definitions required for verification are stated above. The literature comparison places the unsolved $10j$ in its proper context.

---

*This technical note forms part of the demonstrated scientific contribution and is to be read in conjunction with the Final Report of 25 October 2026 and the constituent repositories.*