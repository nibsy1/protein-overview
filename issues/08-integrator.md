# Integrator with explicit conflict flagging

## Summary
Merges the parallel harvesters' outputs into the store, flagging every conflict explicitly.

## Details
- Conflicts (e.g. ECA3 localization: Golgi vs endosome/PVC vs TGN) are recorded as competing claims with sources — never silently resolved.
- Normalizes tiers; ensures every claim has a source and exactly one tier before handoff to the hypothesis generator.

## Acceptance criteria
- ECA3 store shows the localization conflict as competing claims from Mills 2008 / Li 2008 / Farthing 2023.

Ref: PRD §3
