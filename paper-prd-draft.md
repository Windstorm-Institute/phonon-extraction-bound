# Submission scaffold — Physical Review D

**Title:** A Non-Equilibrium Efficiency Bound for Phonon Extraction in Bose–Einstein Condensate Analog Gravity Systems with Numerical Tests of the Underlying Thermodynamic Assumption

**Author:** Grant Lavell Whitmer III, The Windstorm Institute, Fort Ann, NY 12827, USA · grantwhitmer3@gmail.com

**PACS / PhySH:** Analog gravity · Bose–Einstein condensates · Non-equilibrium thermodynamics · Holographic screens · Lindblad master equation

**Suggested section:** Section IV — General Relativity, Cosmology, and Astrophysics → Analog gravity. Alternative: Section II — Quantum Foundations, Quantum Information, Holography.

---

## Cover-letter abstract

We apply standard non-equilibrium thermodynamics to a Verlinde-style holographic screen entropy and obtain, under one explicit thermodynamic assumption, an efficiency bound η ≤ 1 − T/T_res for processes that displace excitations against an effective gravitational potential. The bound becomes restrictive only in the regime T/T_res ~ O(1) — accessible in BEC analog gravity but not in any astrophysical setting. For laboratory BEC parameters the bound predicts a 20% efficiency suppression at T/T_res = 0.2, distinguishable from naive energetic accounting and from mundane experimental losses by its specific functional form. The central substitution is examined numerically across five settings of QuTiP Lindblad simulations, which for thermal states are consistency checks on the integrator (the substitution is then an identity) rather than independent tests, with the numerical method fully specified (the scripts are not yet publicly archived). We do not modify gravitational dynamics, do not propose a new theory of gravity, and do not claim a derivation. We claim only a falsifiable laboratory signature.

---

## What's in this repo

- `paper.pdf` — full manuscript (current v1.0)
- `paper/Paper10-v1.0-draft.md` — markdown source
- `paper-arxiv.tex` — arXiv submission scaffold (gr-qc / quant-ph)
- `article.html` — long-form companion article (also at windstorminstitute.org)

## Reviewer reproducibility statement

All numerical tests in Section 3 are reproducible with QuTiP 5.2.3 in standard Python 3.12 environments. Total compute is ~30 minutes on a single CPU. The simulation scripts and raw logs are not yet publicly archived; the numerical method is fully specified in Section 3, and the scripts will be released in the companion Windstorm Labs repository.
