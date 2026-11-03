# Benchmark Panel — Functional-Characterization Workflow

Fixed evaluation set, defined **before** agent implementation (PRD §9.1).
Accessions are intentionally resolved by the pipeline itself — entity resolution
is part of what is being scored. Gold annotations are established, textbook-level
functional knowledge used to score hypothesis recall/precision.

| # | Organism (clade) | Gene | Role class | Gold-standard annotations (recall targets) |
|---|---|---|---|---|
| 1 | *Homo sapiens* (human) | TP53 | transcription factor | Tumor suppressor TF; cell-cycle arrest, apoptosis, DNA-damage response; mutated in most cancers |
| 2 | *Homo sapiens* (human) | ATP2A2 (SERCA2) | enzyme / ion pump | ER/SR Ca2+-ATPase (P2B); pumps Ca2+ into ER; theme link to ECA3; mutations → Darier disease |
| 3 | *Mus musculus* (mouse) | Pax6 | developmental TF | Paired-box TF; eye, pancreas, CNS development; MGI mutant phenotypes |
| 4 | *Danio rerio* (zebrafish) | sox10 | developmental TF | Neural crest / glial development TF; ZFIN mutant phenotypes |
| 5 | *Drosophila melanogaster* (fly) | dpp | morphogen (BMP) | Secreted BMP morphogen; dorsal-ventral patterning; FlyBase alleles |
| 6 | *Caenorhabditis elegans* (worm) | daf-2 | receptor (insulin/IGF-1) | Insulin/IGF-1 receptor; dauer formation, longevity, stress resistance |
| 7 | *Saccharomyces cerevisiae* (fungus) | GAL4 | transcription factor | Master activator of galactose (GAL) regulon; well-characterized DNA binding |
| 8 | *Saccharomyces cerevisiae* (fungus) | PMA1 | enzyme / H+-ATPase | Plasma membrane H+-ATPase (P3A); major proton pump, essential gene |
| 9 | *Arabidopsis thaliana* (plant) | FLC (AT5G10140) | transcription factor | MADS-box floral repressor; vernalization; flowering time control |
| 10 | *Arabidopsis thaliana* (plant) | ECA3 (AT1G10130) | transporter / Ca2+-ATPase | **Reference case.** P2A Golgi/post-Golgi Ca2+/Mn2+ pump; Mn nutrition; eca3 mutant phenotypes |
| 11 | *Oryza sativa* (plant) | OsECA3 (Os03g52090) | transporter | ECA3 ortholog; tests multi-candidate resolution + ortholog extrapolation |
| 12 | *Plasmodium falciparum* (protist) | MSP1 | surface protein | Merozoite surface protein 1; erythrocyte invasion, malaria vaccine candidate |

## Scoring per benchmark protein
- **Recall**: fraction of gold annotations surfaced as claims/hypotheses with correct tier.
- **Precision**: zero fabricated citations/accessions/claims (hard fail otherwise).
- **Completeness**: all fixed report sections present; gaps explicitly marked.
- **Discriminability**: each hypothesis has ≥1 proposed experiment that distinguishes it from the top alternative.
