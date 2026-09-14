# Stanley growth as inverse mean oriented-reflection multiplicity

**Author:** Jared Wilder  
**Human extraction:** 2026-09-14  
**Parent status:** the Erdős #271 / `A(4)` asymptotic target remains **OPEN**.

The late audited endpoint of the #271 program is not a theorem about maximum reflection multiplicity. It is an exact dictionary between sequence growth and **mean oriented-reflection multiplicity**.

## Reflection support

For a Stanley sequence `a_0<a_1<...`, define

```text
U_k = { 2a_j-a_i : 0 ≤ i < j < k }.
```

For each integer `x`, define the oriented reflection multiplicity

```text
m_k(x)
  = #{(i,j): 0 ≤ i<j<k, 2a_j-a_i=x}.
```

The mean multiplicity of the occupied support is

```text
μ_k = binom(k,2) / |U_k|.
```

The exact counting identities are

```text
∑_x m_k(x) = binom(k,2),
|U_k| = ∑_x 1_{m_k(x)>0},
Λ_k = ∑_x (m_k(x)-1)_+.
```

Thus greedy Stanley growth can be studied through the geometry and collision multiplicity of the oriented reflection support.

---

## Exact `A(4)` reservoir identity

For `A(4)`, the forced seed omissions are `1,2,3`; they are not represented by the oriented reflection system. Therefore

```text
|U_k ∩ [0,a_k)| = a_k - k - 3.
```

If `Q_k` denotes the future part of the reservoir, then

```text
|U_k| = (a_k-k-3) + Q_k.
```

The support is localized by

```text
U_k ⊂ [1,2a_{k-1}],
```

so

```text
Q_k ≤ max(0, 2a_{k-1}-a_k+1).
```

The seed correction is load-bearing: earlier uncorrected complement identities are not used here.

---

## Half-utilization theorem

Let `η_k` be the used fraction of the reflection reservoir. For every fixed-seed infinite Stanley sequence, the audited theorem gives

```text
liminf_{k→∞} η_k ≥ 1/2.
```

For `A(4)`, the exact multiplicity-utilization formula is

```text
a_k
  = k + 3
    + η_k · binom(k,2)/μ_k.
```

So the future reservoir cannot asymptotically vanish in a way that changes the growth order.

---

## Multiplicity-only growth theorem

For every fixed seed,

```text
a_k = Θ( k + k²/μ_k ).
```

Using the external fact that every infinite 3-AP-free set has zero density, hence every infinite Stanley sequence is superlinear,

```text
a_k/k → ∞,
```

this simplifies to

```text
a_k = Θ(k²/μ_k).
```

The superlinearity input is external. The exact reduction of Stanley growth to `μ_k` is the estate theorem.

---

## `A(4)` target rewritten exactly

Inside this dictionary, the historical target

```text
a_k = Θ(k²/log k)
```

is equivalent to

```text
μ_k = Θ(log k),
```

and equivalently

```text
|U_k| = Θ(k²/log k).
```

More generally, for `1 < α ≤ 2`, the audited ledger gives

```text
a_k = Θ(k^α)
    ⇔
μ_k = Θ(k^(2-α)).
```

Slowly varying factors transport inversely in the same way.

So the asymptotic growth question becomes a reflection-fiber multiplicity question.

---

## Reflection-energy reduction

Cauchy–Schwarz gives

```text
|U_k|
  ≥ binom(k,2)^2 / ∑_x m_k(x)^2.
```

Therefore a sufficiently strong second-moment estimate on the affine self-intersection multiplicities would imply the desired support lower bound. This is the clean analytic minimum cut left by the reduction.

---

## Finite audit and killed route

The dependency-free audit generated 2,049 terms of `A(4)`. At the packaged checkpoints `k=64,...,2048`, the data recorded:

- `μ_k/log k` roughly in the range `0.517–0.589`;
- utilization above `0.51`;
- total maximum multiplicity reaching `21`;
- maximum multiplicity within one ternary distance scale growing through `7,9,10,11,15,19`.

Therefore the proposed **absolute per-scale multiplicity constant** is false. A surviving scale theorem would have to allow slowly growing per-scale multiplicity.

This finite audit is evidence about route structure, not a proof of the `A(4)` asymptotic.

---

## Status

The correct human headline is:

> **Stanley growth is inverse mean oriented-reflection multiplicity.**

The `A(4)` asymptotic remains open. Historical novelty for the reflection/first-kill/multiplicity identities has not been globally adjudicated.
