# Report generator + automated integrity checks

## Summary
Deterministic report generation from the store, plus integrity checks run on every execution.

## Details
- Fixed section order (base skill) extended with Expression & Regulation, Comparative Homology, Hypotheses, Proposed Experiments, Evidence Table, Sources.
- Integrity checks: every claim has a source and exactly one evidence tier; every citation resolves; all conflicts flagged. Violations fail the run.

## Acceptance criteria
- Report for Q9SY55 regenerates deterministically from store files; integrity check suite passes; a seeded bad claim fails the run.

Ref: PRD §2, §8; skill Stage 4
