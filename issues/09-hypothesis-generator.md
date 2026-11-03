# Hypothesis generator (ortholog + family templates + mechanism-first)

## Summary
Systematic generation of 3–8 ranked, falsifiable functional hypotheses per protein.

## Details
- Generators: (1) well-supported functions of closest characterized ortholog (tier [d] until tested in organism), (2) protein-family functional templates (substrate, compartment, regulation, mutant phenotype for a P-type ATPase), (3) mechanism-first derivation from sequence/structure.
- Ranked by evidence strength and discriminability (can an experiment tell it apart from the top alternative?).

## Acceptance criteria
- ECA3 run yields ranked hypotheses (e.g. "Golgi/TGN Ca2+/Mn2+ loading for Mn nutrition" vs "endosomal Mn detoxification/secretory role") each with tier labels and confidence.

Ref: PRD §3
