# Resolver agent with multi-candidate output

## Summary
Entity-resolution agent: normalize any input (UniProt accession, gene name, protein name, PDB ID, bare sequence) to canonical identifiers and emit a candidate set.

## Details
- Output canonical identifiers: UniProt primary accession, gene symbol, organism, NCBI taxon ID.
- Ambiguity: proceed with ALL plausible candidates (never silently guess); log choice rationale in decision-log.md.
- Bare sequence: homology-based identification with best-match scores.
- Hard stops: prokaryotic/viral protein (out of scope) or zero resolvable canonical identifier.

## Acceptance criteria
- "ECA3" resolves to a candidate set containing AT1G10130/Q9SY55 and Os03g52090; decision log written.

Ref: PRD §7; skill Stage 0
