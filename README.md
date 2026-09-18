# Erdős #271 — Stanley sequences and reflection multiplicity

Let

\[
a_0<a_1<a_2<\cdots
\]

be a Stanley sequence. This repository gives an exact dictionary between its growth and the mean multiplicity of the oriented reflection set

\[
U_k=\{2a_j-a_i:0\le i<j<k\}.
\]

The central result is that, for every fixed seed,

\[
\boxed{a_k=\Theta\!\left(k+\frac{k^2}{\mu_k}\right),}
\]

where

\[
\mu_k=\frac{\binom{k}{2}}{|U_k|}
\]

is the mean multiplicity of the occupied reflection support.

Using the classical fact that every infinite 3-term-progression-free set has zero density, hence every infinite Stanley sequence is superlinear, this simplifies to

\[
\boxed{a_k=\Theta\!\left(\frac{k^2}{\mu_k}\right).}
\]

## The `A(4)` problem becomes a multiplicity problem

For the Stanley sequence generated from the seed `A(4)`, the historical target

\[
a_k=\Theta\!\left(\frac{k^2}{\log k}\right)
\]

is therefore equivalent, within this framework, to

\[
\boxed{\mu_k=\Theta(\log k),}
\]

and equivalently to

\[
\boxed{|U_k|=\Theta\!\left(\frac{k^2}{\log k}\right).}
\]

More generally, for `1<\alpha\le2`, the same dictionary gives

\[
a_k=\Theta(k^\alpha)
\iff
\mu_k=\Theta(k^{2-\alpha}).
\]

So the growth problem can be studied as a question about how often distinct ordered pairs `(i,j)` produce the same reflection value `2a_j-a_i`.

## Exact counting identities

Define

\[
m_k(x)=\#\{(i,j):0\le i<j<k,\ 2a_j-a_i=x\}.
\]

Then

\[
\sum_x m_k(x)=\binom{k}{2},
\qquad
|U_k|=\sum_x 1_{m_k(x)>0}.
\]

For `A(4)`, the occupied portion of the reflection reservoir below the next Stanley term satisfies the exact identity

\[
|U_k\cap[0,a_k)|=a_k-k-3.
\]

The correction `-3` comes from the forced seed omissions `1,2,3`; it is essential in the exact formula.

The same development proves a half-utilization theorem: if `\eta_k` denotes the fraction of the available reflection reservoir that has already been used, then

\[
\liminf_{k\to\infty}\eta_k\ge\frac12.
\]

For `A(4)`, this yields

\[
a_k
=
k+3+
\eta_k\frac{\binom{k}{2}}{\mu_k}.
\]

## A second-moment route

Cauchy–Schwarz gives

\[
|U_k|
\ge
\frac{\binom{k}{2}^2}{\sum_x m_k(x)^2}.
\]

Thus a sufficiently strong upper bound on the reflection energy

\[
\sum_x m_k(x)^2
\]

would imply the support lower bound needed for the expected `A(4)` growth. This is the clean analytic bottleneck exposed by the reduction.

## Finite computation

The source audit generated the first **2,049 terms** of `A(4)` and measured the reflection statistics at powers of two through `k=2048`.

Across the packaged checkpoints:

- `\mu_k/\log k` lies roughly between `0.517` and `0.589`;
- reflection-reservoir utilization stays above `0.51`;
- the maximum total reflection multiplicity reaches `21`;
- the maximum multiplicity inside one ternary distance scale grows through `7,9,10,11,15,19`.

The last observation refutes an earlier proposed route that required an absolute constant bound on per-scale multiplicity. Any successful scale-by-scale argument must allow slow growth.

These computations support the structural picture; they are not being used as a proof of the asymptotic.

## Read the full derivation

[`REFLECTION-MULTIPLICITY-GROWTH.md`](REFLECTION-MULTIPLICITY-GROWTH.md) contains the exact reservoir identities, half-utilization theorem, multiplicity-growth dictionary, energy reduction, and finite audit.

Historical research records remain under `source/`. The source ledger contains many intermediate claims and diagnostics, but the reflection-multiplicity theorem above is the recommended mathematical entry point.

Historical priority for the reflection formulation has not yet been fully adjudicated.

Author: Jared Wilder.