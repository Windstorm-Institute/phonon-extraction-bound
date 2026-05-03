# Paper 10: A Non-Equilibrium Efficiency Bound for Phonon Extraction in BEC Analog Gravity

**A Non-Equilibrium Efficiency Bound for Phonon Extraction in Bose–Einstein Condensate Analog Gravity Systems with Numerical Tests of the Underlying Thermodynamic Assumption**

Grant Lavell Whitmer III · Windstorm Labs, The Windstorm Institute · Fort Ann, NY, USA

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey)](https://creativecommons.org/licenses/by/4.0/)
[![Status: Preprint](https://img.shields.io/badge/Status-Preprint-orange)](https://github.com/Windstorm-Institute/phonon-extraction-bound)

**Zenodo**: DOI pending · **Current version: v1.0** (May 2026)

---

## What this paper claims

Apply the Clausius inequality to a two-temperature process — a system at the local analog Unruh temperature `T` coupled to an energy reservoir at temperature `T_res` — with the entropy change on a holographic-style screen taken from Verlinde's expression. Under one explicit thermodynamic assumption (Assumption A: the screen exchanges heat reversibly with its immediate environment while the reservoir coupling carries the irreversibility), the maximum extraction efficiency is

```
η ≤ 1 / (1 + T/T_res)
```

For laboratory BEC parameters (`T_res ~ 50 nK`, `T_analog ~ 10 nK`), the bound predicts `η ≤ 0.83` — a 17% suppression below the naive energetic expectation. The regime `T/T_res ~ O(1)` is accessible in BEC analog gravity but not in any astrophysical setting, which is where the bound has empirical content distinguishable from standard energy accounting.

Assumption A is tested numerically across five independent dimensions via QuTiP Lindblad master-equation simulations (timestep convergence, system size, coupling strength, two-bath driven non-equilibrium steady states, non-thermal initial states). The substitution holds within numerical error for thermal initial states across `T/T_res ∈ [0.20, 0.50]` in both qubit and bosonic-mode systems, with `O(dt)` convergence. It fails for non-thermal initial states with macroscopic coherences — a clean limit on scope.

The paper does **not** modify Newtonian or general-relativistic gravity, does not derive a new equation of motion, and does not claim a unification of entropy and gravity. It claims only a falsifiable laboratory signature in cold-atom analog gravity.

## Read the Paper

- **[paper.pdf](paper.pdf)** — full academic paper
- **[paper/Paper10-v1.0-draft.md](paper/Paper10-v1.0-draft.md)** — markdown source
- **[Website article](https://windstorminstitute.org/articles/phonon-extraction-bound.html)** — long-form companion

## Falsification protocol (Section 6)

The framework is falsified if a controlled BEC analog gravity experiment with `T/T_res` varied across `[0.05, 0.5]` produces phonon extraction efficiencies that:

1. Exceed the bound by more than experimental uncertainty.
2. Show no scaling with `T/T_res`.
3. Show scaling with `T/T_res` but with a functional form inconsistent with `η = 1/(1 + T/T_res)`.

A confirmation outcome — efficiency suppressed by ~17% at `T/T_res = 0.2`, scaling correctly across the accessible range, surviving independent calibration of mundane loss channels — would constitute the first laboratory-scale evidence that holographic-screen entropy of the Verlinde (2011) type has thermodynamic content beyond the equilibrium force law.

## Reproducibility

Numerical tests in Section 3 use QuTiP 5.2.3. Total compute cost across all reported tests is approximately 30 minutes on a standard CPU. Simulation code, raw output logs, and convergence diagnostics are archived alongside this paper (see Data Availability section in the paper).

---

## The Windstorm Institute — Two Research Tracks

### Track 1 — The Throughput Basin (information theory across substrates)

| # | Paper | DOI |
|---|-------|-----|
| 1 | [The Fons Constraint](https://github.com/Windstorm-Institute/fons-constraint) | [10.5281/zenodo.19274048](https://doi.org/10.5281/zenodo.19274048) |
| 2 | [The Receiver-Limited Floor](https://github.com/Windstorm-Institute/receiver-limited-floor) | [10.5281/zenodo.19322973](https://doi.org/10.5281/zenodo.19322973) |
| 3 | [The Throughput Basin](https://github.com/Windstorm-Institute/throughput-basin) | [10.5281/zenodo.19323194](https://doi.org/10.5281/zenodo.19323194) |
| 4 | [The Serial Decoding Basin τ](https://github.com/Windstorm-Institute/serial-decoding-basin) | [10.5281/zenodo.19323423](https://doi.org/10.5281/zenodo.19323423) |
| 5 | [The Dissipative Decoder](https://github.com/Windstorm-Institute/dissipative-decoder) | [10.5281/zenodo.19433048](https://doi.org/10.5281/zenodo.19433048) |
| 6 | [The Inherited Constraint](https://github.com/Windstorm-Institute/inherited-constraint) | [10.5281/zenodo.19432911](https://doi.org/10.5281/zenodo.19432911) |
| 7 | [The Throughput Basin Origin](https://github.com/Windstorm-Institute/throughput-basin-origin) | [10.5281/zenodo.19498582](https://doi.org/10.5281/zenodo.19498582) |
| 8 | [The Vision Basin](https://github.com/Windstorm-Institute/vision-basin) | [10.5281/zenodo.19672827](https://doi.org/10.5281/zenodo.19672827) |
| 9 | [The Hardware Basin](https://github.com/Windstorm-Institute/hardware-basin) | [10.5281/zenodo.19672921](https://doi.org/10.5281/zenodo.19672921) |

### Track 2 — Entropic Bounds in Analog Systems (newly opened)

| # | Paper | DOI |
|---|-------|-----|
| 10 | [Phonon Extraction Bound (BEC Analog Gravity)](https://github.com/Windstorm-Institute/phonon-extraction-bound) | DOI pending |

**Website:** [windstorminstitute.org](https://windstorminstitute.org)

---

*License: MIT (code) and CC BY 4.0 (data, figures, paper text). See [LICENSE](LICENSE).*
