# A Non-Equilibrium Efficiency Bound for Phonon Extraction in Bose–Einstein Condensate Analog Gravity Systems with Numerical Tests of the Underlying Thermodynamic Assumption

**Grant L. Whitmer III**
*Windstorm Institute, Fort Ann, New York*
[contact information]

---

## Abstract

We derive a non-equilibrium efficiency bound for processes that displace excitations against an effective gravitational potential in a Bose–Einstein condensate (BEC) analog gravity system. The bound applies the Clausius inequality to a two-temperature process: a system at the local analog Unruh temperature $T$ coupled to an energy reservoir at temperature $T_{\rm res}$, with the entropy change on a holographic-style screen taken from Verlinde's expression. Under one explicit thermodynamic assumption — that the screen exchanges heat with its immediate environment in a locally reversible manner ($\delta Q = T\,dS$) while the coupling to the reservoir carries the irreversibility — the predicted maximum extraction efficiency is

$$\eta \leq \frac{1}{1 + T/T_{\rm res}}.$$

For laboratory BEC parameters ($T_{\rm res} \sim 50$ nK, $T_{\rm analog} \sim 10$ nK), the bound predicts $\eta \leq 0.83$, a 17% suppression below the naive energetic expectation of $\eta \approx 1$. We argue that the regime $T/T_{\rm res} \sim O(1)$ — accessible in BEC analog gravity but not in any astrophysical setting — is where this bound has empirical content distinguishable from standard energy accounting. The central thermodynamic assumption is tested numerically through a series of Lindblad master-equation simulations across five independent dimensions (timestep convergence, system size, coupling strength, two-bath driven non-equilibrium steady states, and initial-state structure). The simulations support the assumption in the regime $T/T_{\rm res} \geq 0.20$ for thermal-like initial states in both qubit and bosonic-mode systems, with the simulation source code archived and reproducible. We do not modify Newtonian or general-relativistic gravity, do not derive a new equation of motion, and do not claim a unification of entropy and gravity. We claim only that the framework, within its stated scope, predicts a falsifiable laboratory signature in cold-atom analog gravity that distinguishes it from naive energetic accounting.

**Keywords:** entropic gravity, analog gravity, Bose–Einstein condensates, non-equilibrium thermodynamics, Lindblad simulations, Unruh effect

---

## 1. Introduction

Verlinde (2011) proposed that gravitational attraction emerges as an entropic force from information gradients on holographic screens, with the screen entropy change for radial displacement of a test mass $m$ given by

$$dS_{\rm screen} = -2\pi k_B \frac{m c}{\hbar}\,dr. \tag{1}$$

This construction recovers Newtonian dynamics under reversible assumptions. It does not address the irreversible thermodynamic cost of resisting the entropic force when the energy supply has finite temperature. The same gap exists in Jacobson's (1995) earlier derivation of the Einstein field equations from the equilibrium Clausius relation.

This paper takes a narrow approach to that gap. We do not propose a new theory of gravity. We do not modify gravitational dynamics. We ask a single question: *given Verlinde's screen entropy and standard non-equilibrium thermodynamics applied to a two-temperature process, what efficiency bound results, and where can it be tested?* The answer is a Clausius-type inequality. We are explicit throughout that this inequality is not, in itself, novel physics — it follows from combining (1) with the second law applied to processes coupling two thermal reservoirs, under one substantive assumption that we identify, defend, and test numerically in Sections 2 and 3.

The paper's potentially novel content is twofold: first, the *specific functional form* of the resulting efficiency bound, and second, the identification of cold-atom analog gravity as the regime where this functional form becomes restrictive and experimentally testable. Real gravitational systems sit in a parameter regime ($T/T_{\rm res} \ll 1$) where the bound is loose and indistinguishable from the second law. Bose–Einstein condensate analog gravity systems sit in a regime ($T/T_{\rm res} \sim O(1)$) where the bound becomes restrictive and predicts a measurable deviation from naive energetic accounting.

The paper is organized as follows. Section 2 derives the inequality with explicit attention to the central thermodynamic substitution. Section 3 presents numerical tests of that substitution across five independent dimensions. Section 4 derives the efficiency bound and the quantitative BEC prediction. Section 5 discusses the bound's relationship to astrophysical and engineering systems. Section 6 outlines a falsification protocol. Section 7 lists limitations honestly. Section 8 concludes.

---

## 2. Derivation of the Non-Equilibrium Bound

### 2.1 Setup

We consider a process in which energy is supplied by a reservoir at temperature $T_{\rm res}$ to extract a phonon excitation from an effective acoustic well in a BEC, or — by direct analog — to displace a test mass radially outward against a gravitational potential. The local screen temperature is the Unruh temperature

$$T = \frac{\hbar a}{2\pi c k_B}, \tag{2}$$

where $a$ is the proper acceleration. For acoustic analog systems, $c$ is replaced by the local sound speed $c_s$ and $a$ by the effective surface gravity $g_{\rm eff}$ derived from the condensate's density gradient (Unruh 1981; Barceló, Liberati & Visser 2005).

### 2.2 Two-temperature Clausius inequality

The Clausius inequality for a process exchanging heat $\delta Q_{\rm res}$ with the reservoir and depositing heat $\delta Q_{\rm screen}$ at the screen reads

$$dS_{\rm prod} = \frac{\delta Q_{\rm screen}}{T} - \frac{\delta Q_{\rm res}}{T_{\rm res}} \geq 0. \tag{3}$$

Energy conservation requires

$$\delta Q_{\rm res} = \delta Q_{\rm screen} + dE_{\rm extracted}, \tag{4}$$

where $dE_{\rm extracted}$ is the useful work extracted from the process.

### 2.3 The screen-reversibility assumption

The standard derivation in entropic gravity invokes the substitution

$$\delta Q_{\rm screen} = T \cdot |dS_{\rm screen}|. \tag{5}$$

This substitution holds rigorously only for reversible heat exchange at temperature $T$. In a non-equilibrium setting, where the process driving the screen's entropy change is itself irreversible, the substitution requires a separation of timescales: the screen, treated as a thermal subsystem, equilibrates rapidly compared to the timescale of the displacement process, exchanging heat reversibly at temperature $T$ with its immediate environment, while the *coupling* between reservoir and combined system carries the irreversibility.

We label this Assumption (A) and treat it as load-bearing. The empirical content of the paper is conditional on (A): the BEC prediction in Section 4 follows under (A); the experiment proposed in Section 6 tests (A) and the underlying construction simultaneously. Section 3 reports numerical tests of (A) in a class of Lindblad-equation models.

### 2.4 The bound

Substituting (5) into (3) and using (4) yields, after rearrangement,

$$dS_{\rm prod} \geq \frac{T}{T_{\rm res}}\,|dS_{\rm screen}| - \frac{dE_{\rm extracted}}{T_{\rm res}}. \tag{6}$$

Defining the extraction efficiency $\eta = dE_{\rm extracted}/dE_{\rm input}$, where $dE_{\rm input}$ is the total energy supplied by the reservoir, and using

$$dE_{\rm input} = T\,|dS_{\rm screen}| + T_{\rm res}\,dS_{\rm prod}, \tag{7}$$

together with the saturation condition $dS_{\rm prod} \to 0$ that maximizes extraction efficiency, we obtain

$$\boxed{\eta \leq \frac{1}{1 + T/T_{\rm res}}}. \tag{8}$$

This is the central result.

### 2.5 Reversible and strong-coupling limits

In the reversible limit $T_{\rm res} \to \infty$, equation (8) gives $\eta \to 1$ and standard conservative mechanics is recovered. In the strong-coupling limit $T_{\rm res} \to T$, the bound predicts $\eta \to 1/2$. The regime $T_{\rm res} < T$ is unphysical for the standard second-law setup considered here.

---

## 3. Numerical Tests of Assumption (A)

We tested Assumption (A) in a series of open-quantum-system simulations using the QuTiP library (Johansson, Nation & Nori 2013; QuTiP 5.2.3). The strategy throughout: construct minimal Lindblad models in which the substitution $\delta Q = T \cdot dS$ can be checked directly against numerically computed heat and entropy changes, then probe the substitution along five independent dimensions. The simulation code, raw output logs, and convergence diagnostics are archived alongside this paper (see Data Availability).

Each test was specified before execution and reported in full, including failures. Two tests revealed numerical or setup defects in their initial form (one timestep-resolution issue, one Hamiltonian-sign-convention issue) that were corrected in subsequent runs; the failures are documented along with the corrections in the supplementary material. No test outcome was modified post hoc to favor the assumption.

### 3.1 Test 1: Timestep convergence (single-qubit baseline)

A single qubit with Hamiltonian $H = -\frac{1}{2}\omega\sigma_z$ was coupled to a thermal reservoir at $T_{\rm res} = 1.0$ via Lindblad operators $\sqrt{\gamma(n_{\rm th}+1)}\sigma_-$ and $\sqrt{\gamma n_{\rm th}}\sigma_+$, with $\gamma = 0.05$ and $\omega = 1.0$ in natural units. Initial states were thermal at $T = r \cdot T_{\rm res}$ for $r \in \{0.05, 0.10, 0.20, 0.30, 0.50\}$. The ratio $\delta Q / (T \cdot dS)$ was computed for timesteps $dt \in \{10^{-2}, 10^{-3}, 10^{-4}, 10^{-5}\}$.

**Result.** For $r \geq 0.10$, the ratio converges monotonically to 1.000 within 0.1% as $dt \to 10^{-5}$. At $r = 0.05$ the ratio is still drifting downward at $dt = 10^{-5}$ (value 1.331, fractional change 15% between the smallest two timesteps), with $dS$ verified to be 595,000 times above the floating-point noise floor — indicating real physical (not numerical) finite-step dependence at very low temperature ratios.

**Convergence-order analysis.** Power-law fits of $|\text{ratio} - 1|$ versus $dt$ over the range $dt \leq 0.1$ yield exponents $\alpha = 0.999$ at $r = 0.50$ ($R^2 = 1.0000$), $\alpha = 0.993$ at $r = 0.30$, $\alpha = 0.960$ at $r = 0.20$, $\alpha = 0.526$ at $r = 0.10$, and $\alpha = 0.211$ at $r = 0.05$. The clean $O(dt)$ scaling for $r \geq 0.20$ is consistent with first-order Trotter error in the integrated Lindblad evolution. The sub-linear scaling at $r \leq 0.10$ indicates that the approach to the continuum limit is genuinely slower in the near-pure-state regime, where short-time entropy production contains non-analytic small-eigenvalue corrections.

### 3.2 Test 2: Bosonic mode (truncated harmonic oscillator)

The qubit was replaced with a truncated harmonic oscillator ($N = 10$ levels) — the natural model for a phonon mode in a BEC. Hamiltonian $H = \omega \cdot a^\dagger a$, dissipators $\sqrt{\gamma(n_{\rm th,bath}+1)}\,a$ and $\sqrt{\gamma n_{\rm th,bath}}\,a^\dagger$. Initial state thermal at $T = r \cdot T_{\rm res}$ for $r \in \{0.10, 0.20, 0.30, 0.50\}$, timesteps $dt \in \{0.5, 0.1, 0.01, 0.001\}$.

**Result.** Truncation at $N = 10$ verified safe across all parameter values (maximum population at level 9 below $4 \times 10^{-8}$). At $dt = 10^{-3}$, the ratio is $1.0275$ at $r = 0.10$, $1.0004$ at $r = 0.20$, $1.0001$ at $r = 0.30$, and $1.0000$ at $r = 0.50$ — indistinguishable from the qubit case in the same regime. Convergence-order analysis yields $\alpha = 0.999$ at $r = 0.50$, $\alpha = 0.997$ at $r = 0.30$, $\alpha = 0.986$ at $r = 0.20$, and $\alpha = 0.630$ at $r = 0.10$ — again clean $O(dt)$ for $r \geq 0.20$ and sub-linear at $r = 0.10$, mirroring the qubit pattern.

**This test addresses the most physically relevant generalization for the BEC application**, where phonon modes are the natural degree of freedom. The substitution holds with the same convergence structure as the qubit case.

### 3.3 Test 3: Strong-coupling regime

The qubit setup was repeated with $\gamma \in \{0.05, 0.5, 1.0, 2.0\}$, sweeping from the weak-coupling regime ($\gamma/\omega = 0.05$) into territory ($\gamma/\omega = 2$) where standard Markovian Lindblad assumptions become questionable. Timestep $dt = 10^{-4}$.

**Result.** For $r \geq 0.30$, the ratio remains within 0.1% of 1.000 across the entire range of $\gamma/\omega$, even at the strong-coupling endpoint. At $r = 0.10$, the ratio rises monotonically from 1.005 at $\gamma = 0.05$ to 1.119 at $\gamma = 2.0$. **The substitution is robust to strong coupling at moderate temperature ratios but degrades when both the coupling is strong and the temperature ratio is small.** The BEC application sits comfortably in the weak-coupling regime ($\gamma/\omega \ll 1$ for typical condensate-phonon couplings), so this constraint does not affect the paper's claim within its stated scope.

### 3.4 Test 4: Two-bath driven non-equilibrium steady state

A qubit was coupled simultaneously to a hot bath at $T_{\rm hot} = 1.0$ and a cold bath at $T_{\rm cold} = 0.01$, with $\gamma_h = 0.05$ and $\gamma_c \in \{0.005, 0.05, 0.5\}$. The non-equilibrium steady state was found via direct solution of the Lindblad equation. Heat currents were computed directly from the dissipator structure $J_k = \mathrm{Tr}(H \cdot D_k(\rho_{\rm ss}))$ rather than inferred from energy differences, and the entropy current from the hot bath was computed as $dS_{\rm hot} = -\mathrm{Tr}(\log\rho_{\rm ss} \cdot D_{\rm hot}(\rho_{\rm ss}))$.

**Result.** Energy conservation $Q_{\rm in} + Q_{\rm out} = 0$ holds to $\sim 10^{-16}$ across all $\gamma_c$ values. Effective steady-state temperatures are positive and decrease with increasing $\gamma_c$ ($T_{\rm eff}/T_{\rm hot} = 0.94, 0.67, 0.33$), as expected. **The ratio $Q_{\rm in}/(T_{\rm eff} \cdot dS_{\rm hot})$ equals 1.000 exactly in all three cases.** This addresses the most important conceptual concern in the original derivation — that Assumption (A) was being tested only in relaxation, not in genuine driven non-equilibrium settings.

We note explicitly that this exactness may reflect detailed-balance structure built into the standard thermal Lindblad form. This is a feature, not a bug, of the model class: standard analog-gravity calculations use precisely this Lindblad framework, so the test confirms that the substitution holds within the framework most likely to be applied to a real BEC experiment. Whether it would hold beyond detailed-balance Lindblad models — for example, in the presence of non-Markovian memory effects or strong-coupling reaction-coordinate treatments — is outside the scope of this paper.

### 3.5 Test 5: Non-thermal initial states (negative result)

The qubit setup was repeated with the initial state replaced by the coherent superposition $|+\rangle = (|0\rangle + |1\rangle)/\sqrt{2}$, which has zero von Neumann entropy and maximum off-diagonal coherence. The expectation $\langle\sigma_x\rangle$ was tracked to confirm coherence remained physically present during evolution.

**Result.** The ratio takes values $1.37$, $0.43$, $0.21$ at $r = 0.10, 0.30, 0.50$ — far from 1, strongly $r$-dependent, and inconsistent with Assumption (A). $\langle\sigma_x\rangle$ remained near 1.0 throughout the short evolution, confirming the coherence is real and not a numerical artifact.

**Assumption (A) fails for non-thermal initial states with macroscopic quantum coherences.** This is a meaningful constraint and we do not minimize it. The framework presupposes that the system entering the non-equilibrium process is in or near a thermal state. Phonon modes in a thermalized BEC condensate naturally satisfy this condition; coherently prepared atomic superpositions or squeezed acoustic states would not. The proposed BEC experiment in Section 6 should therefore be conducted in regimes where the phonon mode is thermally populated rather than coherently prepared, and we identify this as an explicit experimental requirement.

### 3.6 Summary of numerical evidence

Across five independent test dimensions, Assumption (A) holds exactly (to numerical error) in the dt → 0 limit for thermal initial states across $r \in [0.20, 0.50]$, in both qubit and bosonic-mode systems, with $O(dt)$ convergence and weak dependence on coupling strength up to $\gamma/\omega \approx 2$. It holds exactly in two-bath driven non-equilibrium steady states within the standard detailed-balance Lindblad framework. It fails for non-thermal initial states with macroscopic coherences. At very low temperature ratios ($r \leq 0.10$), convergence to the dt → 0 limit is sub-linear and slow.

The validated regime — thermal initial states, weak-to-moderate coupling, $T/T_{\rm res} \in [0.20, 0.50]$, bosonic or qubit systems — encompasses the parameter range targeted by the BEC analog gravity prediction in Section 4. Within this regime, the numerical evidence supports Assumption (A) and the bound (8) that follows from it.

---

## 4. The BEC Prediction

### 4.1 Analog gravity setup

In a Bose–Einstein condensate with a controlled density gradient, phonon excitations propagate on an effective acoustic metric (Unruh 1981; Barceló, Liberati & Visser 2005). A phonon localized in a region of high condensate density experiences an effective gravitational potential with surface gravity $g_{\rm eff}$ determined by gradients in the local sound speed and condensate density. The associated analog Unruh temperature is

$$T_{\rm analog} = \frac{\hbar\,g_{\rm eff}}{2\pi c_s k_B}, \tag{9}$$

where $c_s$ is the local sound speed in the condensate. The condensate temperature itself, $T_{\rm condensate}$, plays the role of the energy reservoir.

We assume that Verlinde's screen-entropy expression (1), originally derived for real gravitational systems, applies to acoustic analog systems with the substitutions $c \to c_s$ and $m c \to (\text{effective phonon mass-equivalent}) \times c_s$. This transposition is not derived from first principles. Analog gravity is established to reproduce the *kinematics* of curved spacetime (Unruh 1981; Barceló et al. 2005), but whether it reproduces the *thermodynamics* of holographic screens is itself an open question. We treat this transposition as a hypothesis that the proposed BEC experiment tests directly.

### 4.2 Quantitative prediction

We apply the bound (8) with $T = T_{\rm analog}$ and $T_{\rm res} = T_{\rm condensate}$. For laboratory BEC parameters representative of current experimental capability (Steinhauer 2016; Muñoz de Nova et al. 2019):

- Condensate temperature: $T_{\rm condensate} \sim 50$ nK
- Achievable analog Unruh temperature: $T_{\rm analog} \sim 10$ nK
- Resulting ratio: $T/T_{\rm res} = 0.2$

This places the prediction squarely in the regime where Section 3's numerical tests support Assumption (A). The bound predicts a maximum phonon extraction efficiency of

$$\eta_{\rm max} = \frac{1}{1 + 0.2} = 0.833. \tag{10}$$

Naive energetic accounting predicts $\eta_{\rm naive} \approx 1$, with deviations only from mundane experimental losses. The bound's prediction differs from naive accounting by approximately 17 percentage points.

### 4.3 Operational definition of $\eta$

We define $\eta$ as the ratio of extracted phonon energy to input drive energy in a stimulated phonon extraction process: $\eta = E_{\rm phonon,\,extracted}/E_{\rm drive}$. The drive may be a stimulated Bragg scattering pulse, an RF field coupling internal states, or a controlled density-gradient ramp; the specific implementation affects the systematic error budget but not the operational definition.

This choice corresponds to a quantity that has been measured, with various conventions, in published BEC phonon manipulation experiments (Lahav et al. 2010; Steinhauer 2016; Muñoz de Nova et al. 2019). Whether current experimental sensitivities are sufficient to resolve a 17% suppression above the systematic-error floor is a question that can only be settled in dialogue with experimental groups working in this regime; we identify this as a required next step.

### 4.4 Distinguishing from mundane experimental losses

A 17% suppression would be detectable only if it could be cleanly separated from other inefficiencies in BEC phonon manipulation: thermal phonon populations at finite $T_{\rm condensate}$, mode-coupling losses, finite-pulse-width effects, condensate density inhomogeneities. To distinguish a holographic-screen suppression from these mundane losses, the experiment must:

1. **Vary $T/T_{\rm res}$ in a controlled way** by changing $g_{\rm eff}$, $T_{\rm condensate}$, or both. The bound predicts that $\eta(T/T_{\rm res})$ traces the specific functional form $1/(1 + T/T_{\rm res})$ across the accessible range.
2. **Demonstrate the predicted scaling, not merely a constant offset.** A constant offset can be reproduced by any of the mundane loss channels; the specific functional form $1/(1 + T/T_{\rm res})$ cannot.
3. **Calibrate the mundane loss channels independently** through complementary measurements that suppress or null each channel separately.
4. **Maintain thermal-like initial conditions for the phonon mode.** As established in Section 3.5, Assumption (A) fails for coherently prepared non-thermal states. The experiment must work with thermally populated phonon modes, not coherently prepared atomic superpositions or squeezed states.

---

## 5. The Astrophysical Regime

The bound (8) applies, in principle, to any process driving displacement against an entropic gradient under Assumption (A). For astrophysical and engineering systems, the regime $T/T_{\rm res} \ll 1$ generically holds: the local Unruh temperature for any non-extreme gravitational setting is far below the temperature of any plausible energy reservoir.

For a Saturn V launch, the local Unruh temperature corresponding to surface gravity is approximately $4 \times 10^{-20}$ K, while the combustion chamber temperature is approximately $3500$ K, giving $T/T_{\rm res} \sim 10^{-23}$. The bound's prediction $\eta \leq 1/(1 + 10^{-23})$ is indistinguishable from $\eta \leq 1$, the trivial second-law statement. The same is true for hot Jupiter atmospheric escape, stellar winds, and active galactic nuclei jets to within factors of order $10^{10}$ in either direction.

The bound, in this regime, is loose: any system that satisfies the second law will satisfy the bound, regardless of whether the bound's specific functional form captures real physics. We therefore do not present a numerical regression of efficiency margins against $T/T_{\rm res}$ across astrophysical systems as evidence for the framework. The astrophysical comparison is qualitative context: the bound is compatible with known gravitational phenomenology, but compatibility in a regime where the bound is automatically satisfied is not evidence for the framework's specific functional form.

The decisive test is the BEC experiment of Section 4, in the regime where the bound becomes restrictive.

---

## 6. Falsification Protocol

The framework is falsified if a controlled BEC analog gravity experiment with $T/T_{\rm res}$ varied across $[0.05, 0.5]$ produces phonon extraction efficiencies that:

1. **Exceed the bound (8) by more than experimental uncertainty.** Direct violation of the inequality.
2. **Show no scaling with $T/T_{\rm res}$.** Indicates that the holographic-screen substitution does not apply to acoustic analog systems, falsifying the transposition assumed in Section 4.1.
3. **Show scaling with $T/T_{\rm res}$ but with a functional form inconsistent with $\eta = 1/(1 + T/T_{\rm res})$ at the level of experimental error bars.** Indicates that either Assumption (A) is wrong (despite the numerical support in Section 3), the analog Unruh identification is wrong, or the screen-entropy formula does not transpose cleanly.

A confirmation outcome — efficiency suppressed by approximately 17% at $T/T_{\rm res} = 0.2$, scaling correctly across the accessible range, surviving independent calibration of mundane loss channels — would constitute the framework's first non-trivial empirical confirmation in a regime where the bound is restrictive. It would also constitute the first laboratory-scale evidence that holographic-screen entropy has thermodynamic content beyond the equilibrium force law.

---

## 7. Limitations

We name limitations explicitly. Naming them is part of how this paper aims to be defensible.

**(a) Assumption (A) is supported numerically but not derived analytically.** The Lindblad-equation tests of Section 3 confirm the substitution $\delta Q = T\,dS$ within standard detailed-balance thermal Lindblad models for $T/T_{\rm res} \geq 0.20$ with thermal initial states. They do not constitute an analytical proof. A derivation from first principles — whether through fluctuation theorems, reaction-coordinate methods, or direct quantum Boltzmann analysis — would be a substantially stronger result. We do not have one.

**(b) Assumption (A) fails for non-thermal initial states with macroscopic coherences.** This is a clean negative result from Section 3.5 and we do not minimize it. The framework's experimental validity depends on the BEC experiment being conducted with thermally populated phonon modes, not coherently prepared states.

**(c) The transposition of Verlinde's screen entropy from real gravitational systems to BEC acoustic analog systems is assumed, not derived.** Analog gravity reproduces the kinematics of curved spacetime in acoustic systems; whether it reproduces holographic-screen thermodynamics is itself the question the proposed experiment addresses. Failure of the experiment may indicate the transposition fails rather than that the underlying gravitational construction fails.

**(d) The framework predicts an inequality, not an equality.** A non-equilibrium analog of Jacobson's (1995) derivation — relating screen entropy production to a geometric or dynamical quantity *as an equation of state* — would be substantially stronger. We do not have one. The relative-entropy framework developed in the AdS/CFT context (Faulkner et al. 2014) is the most credible existing path toward such a derivation, and we identify it as the natural direction for follow-up theoretical work.

**(e) At very low temperature ratios ($T/T_{\rm res} \leq 0.10$), convergence of the numerical tests is sub-linear in $dt$.** The substitution still appears to head toward exact equality, but the approach is genuinely slow. Either smaller timesteps or analytic short-time expansions are needed for rigorous validation in this regime. The BEC prediction at $T/T_{\rm res} = 0.20$ sits on the safe side of this boundary, but extensions of the experiment to $T/T_{\rm res} < 0.10$ would require further numerical or analytical work.

**(f) The astrophysical comparison in Section 5 is qualitative.** It demonstrates compatibility, not support. The regime $T/T_{\rm res} \ll 1$ makes the bound loose and the comparison non-discriminating.

**(g) The experimental sensitivity required to resolve the predicted 17% suppression has not been formally established.** Section 4.3 indicates that the operational definition of $\eta$ corresponds to a measured quantity in published BEC experiments. Whether the suppression is resolvable above the systematic error floor of any specific experimental setup requires direct dialogue with experimental groups working in this regime.

**(h) Earlier drafts of this work invoked entanglement-erasure interpretations and quantum Landauer-principle language. We have not retained these here** because the language was not doing technical work in the derivation. If equation (8) is empirically confirmed, an entanglement-theoretic re-derivation may eventually be possible, but the present construction does not require it.

---

## 8. Conclusions

We have applied standard non-equilibrium thermodynamics to a Verlinde-style holographic screen entropy and obtained, under one explicit thermodynamic assumption (Assumption A of Section 2.3), an efficiency bound:

$$\eta \leq \frac{1}{1 + T/T_{\rm res}}.$$

The substitution that defines Assumption (A) has been tested numerically across five independent dimensions (Section 3) using QuTiP Lindblad simulations. It holds within numerical error in the dt → 0 limit for thermal initial states across $T/T_{\rm res} \in [0.20, 0.50]$ in both qubit and bosonic-mode systems, with $O(dt)$ convergence and robustness to coupling strength up to $\gamma/\omega = 2$, and exactly in two-bath driven non-equilibrium steady states. It fails for non-thermal initial states with macroscopic coherences — a clean limit on the framework's scope.

We have not modified Newtonian or general-relativistic gravity. We have not derived a new equation of motion. We have not unified entropy and gravity in the sense of Ryu–Takayanagi or the broader entanglement-as-geometry program (Van Raamsdonk 2010; Faulkner et al. 2014). We claim only the following: that the bound, within its numerically-validated scope, predicts a 17% efficiency suppression in BEC analog gravity at $T/T_{\rm res} = 0.2$, distinguishable from naive energetic accounting. This is a falsifiable laboratory prediction in a regime where current experimental capabilities can plausibly access it.

The framework's empirical content stands or falls on this prediction. The astrophysical compatibility of Section 5 is illustrative context, not evidence. A successful BEC test would establish that holographic-screen entropy of the Verlinde (2011) type has thermodynamic content beyond the equilibrium force law — a small but non-trivial empirical result. A failed test would falsify the construction or its acoustic transposition. Either outcome is informative.

Future theoretical work should address: (i) an analytical derivation of Assumption (A) generalizing the Lindblad-model evidence of Section 3; (ii) the validity of transposing screen entropy to acoustic analog systems; (iii) the relation between this non-equilibrium inequality and a putative non-equilibrium equation of state generalizing Jacobson (1995). Future experimental work should establish, in dialogue with active BEC analog gravity groups, the specific implementation and signal-to-noise budget required to distinguish the predicted 17% suppression from mundane experimental losses.

---

## Data Availability

All simulation code, raw output logs, convergence diagnostics, and intermediate working drafts associated with this paper are archived in the supplementary material accompanying this Zenodo deposit. The simulations were run using QuTiP 5.2.3 in standard Python 3.12 environments. Each numerical test reported in Section 3 corresponds to a complete, executable script with verbatim raw output preserved. Failed initial runs and their corrections are included in full to document the iterative nature of the numerical work.

Reproduction requires QuTiP 5.2.3 or equivalent; total compute cost across all reported tests is approximately 30 minutes on a standard CPU.

---

## Methodology Note

This paper was developed iteratively with assistance from large language models (Claude, Grok, Gemini, ChatGPT, Perplexity) used as adversarial review and computational assistance tools. The numerical experiments in Section 3 were executed by code-execution-enabled instances of these models running real Python scripts in sandboxed environments; no quantitative result reported here was generated without verifiable code execution, and at least two independent runs were conducted to cross-check key findings. Earlier drafts of this work contained claims (numerical regressions over astrophysical datasets, modified-gravity force-law extensions, cosmological connections) that were progressively removed during the review process when they could not be defended. The methodology is documented for transparency and to invite scrutiny of the inputs that produced this manuscript.

---

## References

Barceló, C., Liberati, S. & Visser, M. (2005). Analogue gravity. *Living Reviews in Relativity*, **8**, 12.

Bekenstein, J. D. (1973). Black holes and entropy. *Physical Review D*, **7**, 2333.

Faulkner, T., Guica, M., Hartman, T., Myers, R. C. & Van Raamsdonk, M. (2014). Gravitation from entanglement in holographic CFTs. *Journal of High Energy Physics*, **2014**(3), 51.

Hawking, S. W. (1975). Particle creation by black holes. *Communications in Mathematical Physics*, **43**, 199.

Jacobson, T. (1995). Thermodynamics of spacetime: the Einstein equation of state. *Physical Review Letters*, **75**, 1260.

Johansson, J. R., Nation, P. D. & Nori, F. (2013). QuTiP 2: A Python framework for the dynamics of open quantum systems. *Computer Physics Communications*, **184**, 1234.

Lahav, O., Itah, A., Blumkin, A., Gordon, C. & Steinhauer, J. (2010). Realization of a sonic black hole analog in a Bose–Einstein condensate. *Physical Review Letters*, **105**, 240401.

Landauer, R. (1961). Irreversibility and heat generation in the computing process. *IBM Journal of Research and Development*, **5**, 183.

Muñoz de Nova, J. R., Golubkov, K., Kolobov, V. I. & Steinhauer, J. (2019). Observation of thermal Hawking radiation and its temperature in an analogue black hole. *Nature*, **569**, 688.

Ryu, S. & Takayanagi, T. (2006). Holographic derivation of entanglement entropy from AdS/CFT. *Physical Review Letters*, **96**, 181602.

Steinhauer, J. (2016). Observation of quantum Hawking radiation and its entanglement in an analogue black hole. *Nature Physics*, **12**, 959.

Unruh, W. G. (1976). Notes on black-hole evaporation. *Physical Review D*, **14**, 870.

Unruh, W. G. (1981). Experimental black-hole evaporation? *Physical Review Letters*, **46**, 1351.

Van Raamsdonk, M. (2010). Building up spacetime with quantum entanglement. *General Relativity and Gravitation*, **42**, 2323.

Verlinde, E. (2011). On the origin of gravity and the laws of Newton. *Journal of High Energy Physics*, **2011**(4), 29.

