# Erdős #271 — Stanley Sequences

**Jared Wilder**

Structural and computational work on the growth of Stanley sequences.

The project contains a **184-entry audited ledger** together with exact growth identities, reflection-support multiplicity reductions, computational checkpoints, and a compact surviving reduction of the asymptotic problem.

## Reflection-multiplicity reduction

Let

```text
μ_k = binom(k,2) / |U_k|,
U_k = {2a_j-a_i : 0 ≤ i < j < k}.
```

For every fixed seed, the retained theorem gives

```text
a_k = Θ(k + k²/μ_k).
```

Using the external superlinearity input for infinite 3-AP-free sequences, this sharpens to

```text
a_k = Θ(k²/μ_k).
```

Accordingly, the historical `A(4)` target

```text
a_k = Θ(k²/log k)
```

is equivalent, within this dictionary, to

```text
μ_k = Θ(log k)
```

and to

```text
|U_k| = Θ(k²/log k).
```

The reduction is about **mean oriented-reflection multiplicity**. Maximum multiplicity and per-scale multiplicity are separate finite diagnostics; one proposed absolute per-scale bound was falsified during the campaign.

For the cleaned theorem extraction, see [`REFLECTION-MULTIPLICITY-GROWTH.md`](REFLECTION-MULTIPLICITY-GROWTH.md).

## Source

Historical source material is preserved under `source/`, migrated from `jaredwilder/unpublished-math-papers/erdos271-stanley/`.

The full `A(4)` asymptotic remains the open endpoint. The repository’s contribution is the exact reduction above together with the computational and structural evidence surrounding it.