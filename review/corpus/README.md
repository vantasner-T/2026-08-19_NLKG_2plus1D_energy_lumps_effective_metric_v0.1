# P238 portable oracle companion

This directory preserves the complete independently written oracle corpus for
the peer review of Tiziano Fulceri's 19 August 2026 draft. It is deliberately
portable: a future author-maintained companion repository can take this subtree
without inheriting Substrate's claim registry or promotion decisions.

The audit programs test statements and counterexamples, not agreement with
printed outputs. The replacement programs go further: they supply corrected
derivations or a scoped numerical claim that preserves the paper's intended
wave/lump-to-effective-geometry program. Claim assessments and author-ready
replacement language live in `../claims/results.yaml` and
`../repair-guide.md`. The exact repository-primitive transformation
map is `../provenance/solution-reuse-audit.yaml`.

## Python oracles

From this repository root:

```bash
.venv/bin/python review/corpus/sympy_checks.py
.venv/bin/python review/corpus/scipy_checks.py
.venv/bin/python review/corpus/sympy_replacements.py
.venv/bin/python review/corpus/scipy_replacements.py
```

To create the Python environment:

```bash
python3 -m venv .venv
.venv/bin/python -m pip install -r review/corpus/requirements.txt
```

## Lean oracle

The included `lean-toolchain` and `lakefile.lean` pin Lean and mathlib for this
corpus:

```bash
cd review/corpus
lake update
lake build
```

The combined runner at `review/verify.py` executes both Python and Lean
surfaces after these environments are installed.

## Scope

The corpus retains positive identities, exact qualifications, counterexamples,
numerical sign/domain probes, and constructive replacements for P238-S01
through P238-S18. In particular, the replacement files provide the corrected
scoped action, linearized operator, directional impedance/index, finite-time
real 2+1D localized sine-Gordon trajectory, explicit `O(ell/L)` gradient
estimate, boosted-family square-root derivation, operational clock/ruler
relations, anisotropic inverse, exact conformal equatorial Kerr map and null
roots, and the composed conditional headline. Literature conclusions remain
explicit prose rather than counterfeit numerical proofs.
