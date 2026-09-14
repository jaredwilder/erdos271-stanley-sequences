# Erdős #271 — Stanley sequences

**Author:** Jared Wilder  
**Status:** audited sequence-growth research program; no claim that the parent problem is fully closed.

This repository is the canonical public home for the estate's #271 Stanley-sequence work. The recovered program contains a **184-entry audited ledger** together with exact growth identities, reflection-support multiplicity reductions, computational checkpoints, failed routes, and terminal obligations.

## Structural endpoint

The retained late-stage reduction relates the growth scale of `a_k` to the **mean oriented-reflection multiplicity**

```text
μ_k = binom(k,2) / |U_k|,
U_k = {2a_j-a_i : 0 ≤ i < j < k}.
```

For every fixed seed, the audited theorem gives

```text
a_k = Θ(k + k²/μ_k),
```

and with the external superlinearity input for infinite 3-AP-free sequences this becomes

```text
a_k = Θ(k²/μ_k).
```

Thus the historical `A(4)` target `a_k = Θ(k²/log k)` is equivalent inside the proved dictionary to `μ_k = Θ(log k)` and to `|U_k| = Θ(k²/log k)`.

This is a statement about **mean support multiplicity**, not maximum multiplicity. The maximum-multiplicity and per-scale-multiplicity data belong to the finite audit and route diagnostics; in fact, the proposed absolute per-scale multiplicity bound was falsified.

Read the human theorem extraction: [`REFLECTION-MULTIPLICITY-GROWTH.md`](REFLECTION-MULTIPLICITY-GROWTH.md).

The `A(4)` asymptotic itself remains open.

## Source layout

Exact historical source bytes are migrated under `source/` from `jaredwilder/unpublished-math-papers/erdos271-stanley/`.

The repository preserves corrections and retired lemmas alongside surviving reductions. Historical novelty is not inferred from an internal `PROVED` or `COURT` label.
