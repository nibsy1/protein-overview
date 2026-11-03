# Harvester: sequence & annotations

## Summary
One of the parallel domain harvesters: sequence, domains, targeting, topology.

## Details
- Sources: UniProt; InterPro/Pfam/PROSITE/SMART; SignalP/DeepTMHMM-type predictions for sorting, transit peptides, topology; TargetP for organelle targeting (plastid/mitochondrial).
- Writes claims into store with tiers; GO annotations captured.

## Acceptance criteria
- Q9SY55 harvest reproduces 998 aa, P2A-type ATPase InterPro/Pfam signature set, GO:0005388/GO:0006816.

Ref: PRD §3, §6
