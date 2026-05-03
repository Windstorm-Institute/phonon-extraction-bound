# Submission scaffold — Entropy (MDPI)

**Title:** A Non-Equilibrium Efficiency Bound for Phonon Extraction in Bose–Einstein Condensate Analog Gravity Systems with Numerical Tests of the Underlying Thermodynamic Assumption

**Author:** Grant Lavell Whitmer III, The Windstorm Institute, Fort Ann, NY 12827, USA · grantwhitmer3@gmail.com

**Section:** Quantum Information / Statistical Physics — Non-equilibrium Thermodynamics

**MSC / arXiv class:** 80A05 (Foundations of thermodynamics and heat transfer); 81P50 (Quantum state estimation, quantum tomography, etc.); gr-qc; quant-ph

---

## Cover-letter abstract

We derive a non-equilibrium efficiency bound for displacement processes against an entropic-gravity-style potential in BEC analog systems. Under one explicit thermodynamic assumption (the screen exchanges heat reversibly while the reservoir coupling carries the irreversibility), the Clausius inequality applied to a two-temperature process yields η ≤ 1/(1 + T/T_res). The bound becomes empirically discriminating only when T/T_res ~ O(1), a regime accessible in cold-atom analog gravity but not in astrophysics. For laboratory BEC parameters the bound predicts a 17% suppression below naive energetic accounting, distinguishable from mundane experimental losses by its specific functional form. The load-bearing assumption is tested across five independent QuTiP Lindblad simulations and shown to hold within numerical error for thermal initial states across T/T_res ∈ [0.20, 0.50], with O(dt) convergence; it fails for non-thermal initial states with macroscopic coherences — a clean scope limit. All simulation code archived.

---

## Why Entropy / MDPI

This paper sits squarely at the intersection of (i) holographic / entropic-gravity construction, (ii) non-equilibrium thermodynamics, and (iii) Lindblad open-quantum-system numerics — a combination Entropy regularly publishes. The paper's central object is not a gravitational result but a thermodynamic inequality whose empirical content has been narrowed to a regime accessible in cold-atom laboratories. The posture is conservative: we name limitations, identify scope boundaries, and present a falsification protocol.

## Suggested reviewers

We do not propose specific reviewers; we welcome any reviewer with expertise in (a) entropic gravity / Verlinde-style derivations, (b) BEC analog gravity / Hawking-radiation analogs, or (c) Lindblad-equation modeling of open systems. Adversarial review on Assumption A is particularly welcome.

## Repo

Full manuscript and reproducible simulation code: https://github.com/Windstorm-Institute/phonon-extraction-bound
