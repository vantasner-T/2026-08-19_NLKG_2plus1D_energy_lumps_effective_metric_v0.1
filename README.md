# From 2+1D Nonlinear Klein–Gordon Energy Lumps to Geodesic Propagation

This repository contains Tiziano Fulceri's paper
*From 2+1D Nonlinear Klein–Gordon Energy Lumps to Geodesic Propagation in an
Effective Metric Induced by Substrate Inhomogeneity, Anisotropy and Flow*,
version 0.1 (corrected), dated 19 August 2026.

The manuscript develops a proposed extension of a 1+1D sine–Gordon continuum
construction to a real nonlinear Klein–Gordon field in two spatial dimensions.
Its central ingredients are a material derivative for substrate flow, scalar
inertial density, a symmetric positive-definite stiffness tensor, localized
energy-carrying field configurations, an adiabatic collective coordinate, and
an effective Lorentzian geometry. The later sections construct acoustic
analogues of equatorial Schwarzschild and Kerr geometry.

## Paper

- [Manuscript PDF](2026-08-19_NLKG_2plus1D_energy_lumps_effective_metric_v0.1.pdf)
- Version: 0.1 (corrected)
- Date: 19 August 2026
- Author: Tiziano Fulceri, AReTech – Advanced Research Technology Consulting
- Collaboration noted in the manuscript: SuperGrok Heavy 4.5 (xAI)

## Claims developed in the paper

The companion corpus indexes the paper as 18 distinct claim units. The table
below summarizes the claims in manuscript order without replacing the paper's
equations, hypotheses, or wording.

| ID | Source | Paper claim |
| --- | --- | --- |
| P238-S01 | pp. 3–4, eqs. (1)–(5) | The material derivative and the proposed 2+1D scalar-field action incorporate substrate flow, inertial density, stiffness anisotropy, and a nonlinear potential. |
| P238-S02 | p. 4, eqs. (6)–(9); p. 6, eq. (21) | Variation of the action gives the displayed field equation and its homogeneous, non-flowing, and constant-background reductions. |
| P238-S03 | pp. 4–5, eqs. (10)–(13) | A determinant-based constitutive condition generalizes scalar impedance matching to anisotropic media. |
| P238-S04 | pp. 5–6, eqs. (14)–(20) | The acoustic tensor determines the density and stiffness fields and defines a tensorial refractive index. |
| P238-S05 | p. 6, eqs. (21)–(22) | The principal symbol supplies the convective dispersion relation, directional phase speed, and directional refractive index. |
| P238-S06 | pp. 6–7, §4 | Standard existence results and numerical evidence provide finite-energy localized energy lumps for the proposed 2+1D nonlinear field. |
| P238-S07 | p. 7, eq. (23) | When the lump scale is short relative to background gradients, an adiabatic collective-coordinate ansatz describes its motion. |
| P238-S08 | pp. 7–8, eq. (24) | Integrating the field action over a localized profile yields a relativistic square-root particle action in an induced metric. |
| P238-S09 | pp. 7–8, eqs. (25)–(28) | The einbein action reproduces the massive square-root action, admits a massless limit, and yields geodesic motion. |
| P238-S10 | pp. 8–9, eqs. (29)–(32) | The convective wave dispersion relation is the null condition of a contravariant effective metric. |
| P238-S11 | p. 9, eqs. (33)–(38) | Inverting that metric gives the displayed covariant metric in terms of the refractive tensor and substrate flow. |
| P238-S12 | p. 8, §6 consequences | The effective geometry produces time dilation, anisotropic length contraction, free fall, and gravito-inertial equivalence for energy concentrations. |
| P238-S13 | pp. 10–11, eqs. (39), (43)–(49), (53)–(54) | A static anisotropic acoustic tensor reproduces the equatorial Schwarzschild null cone and coordinate speeds. |
| P238-S14 | p. 11, eqs. (50)–(52) | The Schwarzschild acoustic tensor maps to explicit density and stiffness profiles satisfying the constitutive condition. |
| P238-S15 | pp. 12–13, eqs. (55)–(59) | An acoustic metric with azimuthal flow can be matched coefficient by coefficient to equatorial Kerr geometry. |
| P238-S16 | p. 13, eqs. (60)–(67) | A minimal rotating acoustic tensor and azimuthal flow reconstruct Kerr-like geometry and matched constitutive profiles. |
| P238-S17 | p. 14, eqs. (68)–(72) | The rotating model realizes radial and azimuthal characteristic roots, a horizon, an ergoregion, frame dragging, and asymptotic flatness. |
| P238-S18 | pp. 15–16, §9 | The full chain connects a nonrelativistic substrate to localized particles, special-relativistic kinematics, and effective geodesic gravity. |

The exact source wording, dependencies, oracle assignment, and source anchors
are recorded in [the claim inventory](review/claims/inventory.yaml).

## Repository contents

| Path | Contents |
| --- | --- |
| `2026-08-19_NLKG_2plus1D_energy_lumps_effective_metric_v0.1.pdf` | The manuscript under discussion. |
| [`review/peer-review.md`](review/peer-review.md) | Full manuscript-internal peer review, organized claim by claim. |
| [`review/repair-guide.md`](review/repair-guide.md) | Author-ready formulas, wording, and derivation replacements. |
| [`review/literature-audit.md`](review/literature-audit.md) | Audit of the external existence-theorem references used by the paper. |
| [`review/claims/`](review/claims/) | Machine-readable claim inventory and claim-by-claim review records. |
| [`review/corpus/`](review/corpus/) | Standalone SymPy, SciPy, and Lean audit and replacement sources, with pinned dependencies. |
| [`review/verify.py`](review/verify.py) | Combined runner for the claim inventory and executable corpus. |
| [`review/provenance/`](review/provenance/) | Source identity, upstream review lineage, solution-reuse map, and validation records. |

## Reproduce the companion corpus

Python 3 and Lean's `lake` command are required. From the repository root:

```bash
python3 -m venv .venv
.venv/bin/python -m pip install -r review/corpus/requirements.txt
cd review/corpus
lake update
cd ../..
.venv/bin/python review/verify.py
```

Individual programs and formal files are documented in
[`review/corpus/README.md`](review/corpus/README.md).

## Provenance

The PDF is pinned at SHA-256
`7cd35b8c397e874b581ce6da83c05b7047c256439d615d2f05cbbfb33536dd36`.
The review originated in
[Substrate Framework issue #108](https://github.com/vantasnerdan/substrate-framework/issues/108)
and was published and independently reviewed in
[Substrate Framework PR #145](https://github.com/vantasnerdan/substrate-framework/pull/145).

See [LICENSE](LICENSE) for repository licensing terms.
