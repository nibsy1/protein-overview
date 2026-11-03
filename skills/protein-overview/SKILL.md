---
name: protein-overview
description: Basic research skill for the protein deep-research pipeline. Given any eukaryotic protein identifier (UniProt accession, gene name, protein name, PDB ID, or amino-acid sequence), resolve its identity, gather public data from clade-appropriate sources, integrate evidence with explicit tiers, run gap analysis, and emit a standardized knowledge report. Use as Stage 0-4 of the deeper functional-characterization workflow.
---

# Skill: protein-overview

## When to use
Input is a protein identifier of arbitrary type from any eukaryotic organism (animal, plant, fungus, protist). If the input resolves to a prokaryotic or viral protein, stop and report the mismatch.

## Stage 0 — Entity Resolution
- Normalize input to canonical identifiers: UniProt primary accession, gene symbol, organism, NCBI taxon ID.
- Handle isoforms and ortholog/paralog ambiguity explicitly: list plausible candidates, pick the most likely, state the choice and the alternatives. Never silently guess.
- Bare sequence input: homology-based identification; report best matches with scores.

## Stage 1 — Data Acquisition (clade-appropriate routing is mandatory)
- Sequence & annotations: UniProt, InterPro/Pfam, PROSITE, SMART; SignalP/DeepTMHMM-type predictions; TargetP for organelle targeting.
- Literature: PubMed by gene/protein name and species nomenclature; extend to closest model-organism ortholog for non-model species.
- Orthology & evolution: OrthoDB, OMA, PANTHER, eggNOG.
- Expression: route by clade — GTEx/HPA (human), Bgee, MGI, ZFIN, RGD, FlyBase, WormBase, SGD, TAIR / Ensembl Plants+Fungi+Protists / Expression Atlas; SRA-based RNA-seq for non-model species or state that none exists.
- Structure: PDB (experimental), AlphaFold DB (predicted), ModelArchive; assess confidence and disordered regions.
- Function & pathways: GO, KEGG, Reactome, MetaCyc, STRING/BioGRID.
- Phenotype: OMIM/ClinVar/GWAS (human), MGI, FlyBase/WormBase/SGD/TAIR mutant phenotypes; skip silently where the clade has no equivalent.
- If a source is unreachable or empty, retry or find an alternative before recording "absence of data" as a finding.

## Stage 2 — Evidence Integration
- Flag every conflict explicitly. Every claim carries exactly one tier:
  - [a] experimentally verified
  - [b] inferred by similarity / curated
  - [c] computational prediction
  - [d] extrapolated from orthologs
- State when knowledge comes primarily from orthology rather than the organism itself.

## Stage 3 — Gap Analysis & Extrapolation
- Identify what is not known; for understudied organisms, extend with clearly labeled inference from the closest characterized ortholog, noting evolutionary distance.

## Stage 4 — Report Generation (fixed section order)
1. Identity & Organism
2. Literature
3. Sequence & Domains
4. Orthologs & Evolution
5. Expression
6. Structure
7. Function & Interactions
8. Phenotype (where applicable)
9. Open Questions & Controversies
10. Evidence Table
11. Sources

## Global constraints
- Zero tolerance for fabricated citations, accessions, or database claims.
- Never pad sparse non-model-species reports with family-level filler; state the data gap prominently.
- No assuming human biology, human atlases, or human disease relevance for non-human proteins.
- Present competing hypotheses where the field is contested.
- Output language: English.

## Reference implementation
See `reports/ECA3_Q9SY55_report.md` (Arabidopsis ECA3, AT1G10130 / Q9SY55) for a worked example of the full pipeline.
