# Erdős #271 — A-proved atlas deduplication receipt

**Author:** Jared Wilder  
**Purpose:** preserve the canonical denominator and deduplication facts without creating a second, interpretive theorem ledger.

The canonical estate atlas contains **252** rows in domain `erdos-271-stanley` with tier `A_proved`.

A purely syntactic identity pass that removes only source enumeration prefixes such as `R1 —` or `17 —` yields:

- **132 canonical labels**;
- **120 labels represented twice** across the atlas projections;
- **12 labels represented once**.

Source-status distribution after that label collapse, choosing the more detailed source copy when two copies exist:

- `RETAINED_PROVED`: **103** identities;
- `RETAINED_PROVED_WITH_CORRECTION`: **24** identities;
- `COMPUTATIONALLY_VERIFIED_FINITE`: **4** identities;
- `RETAINED_PROVED_SUBSUMED`: **1** identity.

## Authority firewall

This receipt does **not** promote `A_proved` to Lean/kernel authority. In this atlas domain the rows do not carry `has_proof` or `has_lean` flags. The exact historical theorem text and corrections remain controlled by the public source ledger.

In particular, the four `COMPUTATIONALLY_VERIFIED_FINITE` identities remain finite computational statements, not asymptotic theorems.

## Exact public source bytes

The recovered 184-entry audited source ledger is already public and remains the theorem-text authority:

- `source/ledger-001-046.md`
- `source/ledger-047-092.md`
- `source/ledger-093-138.md`
- `source/ledger-139-184.md`

The atlas is a second projection of that program and contains duplicated identities from master-dossier / theorem-ledger ingestion. This receipt records the collapse without rewriting the mathematics.

## Next court

The next publication pass should bind each of the 132 atlas identities to the exact corresponding source-ledger entry and its correction status. Only then should a consolidated theorem map replace the four source-ledger chunks. Historical novelty remains a later, separate court.
