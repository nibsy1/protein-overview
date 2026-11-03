# Protein Overview Report — ECA3 (Arabidopsis thaliana)

**Input identifier:** ECA3
**Report language:** English
**Evidence tiers used throughout:** [a] experimentally verified · [b] curated / inferred by similarity · [c] computational prediction · [d] extrapolated from orthologs

---

## 1. Identity & Organism

| Field | Value | Tier |
|---|---|---|
| Protein name | Calcium-transporting ATPase 3, endoplasmic reticulum-type (ECA3; "endomembrane Ca2+-ATPase 3") | [b] |
| UniProt primary accession | **Q9SY55** (entry ID ECA3_ARATH, reviewed/Swiss-Prot) | [b] |
| Gene symbol / locus | **ECA3** / **AT1G10130** (chromosome 1: 3,310,930–3,322,269, Ensembl Plants) | [b] |
| NCBI Gene ID | 837550 | [b] |
| Organism | *Arabidopsis thaliana* (thale cress), NCBI taxon ID **3702** | [b] |
| Synonyms | ATECA3, T27I1.16, endomembrane calcium ATPase 3; mRNA EU082212; earlier Ler-ecotype clone AJ132388 | [b] |
| Protein length | 998 aa (UniProt canonical); the cloned cDNA ORF was reported as 997 residues — see Open Questions | [b]/[a] |
| Approx. mass | ~110 kDa (calculated from sequence) | [c] |

**Stage 0 ambiguity resolution.** "ECA3" is not unique across eukaryotes in principle, but no human or mouse gene named ECA3 exists (searches return only unrelated genes such as EPHA3, ECI3, EAAT3/SLC1A1). The ECA (endomembrane/ER-type Ca2+-ATPase) family is plant-specific nomenclature; ECA3 homologs exist in other plants (e.g. rice OsECA3). **Chosen target: Arabidopsis thaliana ECA3 (AT1G10130 / Q9SY55)**, the canonical, best-studied ECA3 — consistent with this project's plant-protein scope. Alternatives: ECA3 orthologs in other angiosperms (e.g. *Oryza sativa* Os03g52090 / ABF98693). No isoform issue: a single canonical isoform (AT1G10130.1) is annotated.

## 2. Literature

Primary experimental literature on AtECA3 (all verified):

1. Mills RF, Doherty ML, López-Marqués RL, Weimar T, Dupree P, Palmgren MG, Pittman JK, Williams LE. *ECA3, a Golgi-Localized P2A-Type ATPase, Plays a Crucial Role in Manganese Nutrition in Arabidopsis.* Plant Physiol. 2008;146(1):116–128. doi:10.1104/pp.107.110817. PMC2230566; PMID 18024560. [a]
2. Li X, Chanroj S, Wu Z, Romanowsky SM, Harper JF, Sze H. *A Distinct Endosomal Ca2+/Mn2+ Pump Affects Root Growth through the Secretory Process.* Plant Physiol. 2008;147(4):1675–1689. doi:10.1104/pp.108.119909. PMC2492598; PMID 18567829. [a]
3. Barabasz A, Mills RF, Trojanowska E, Williams LE, Antosiewicz DM. *Expression of AtECA3 in tobacco modifies its responses to manganese, zinc and calcium.* Environ Exp Bot. 2011;72:202–209. [a]
4. Farthing EC et al. *Dissecting the relative contribution of ECA3 and group 8/9 cation diffusion facilitators to manganese homeostasis in Arabidopsis thaliana.* 2023. PMID 37228331. [a]
5. Wu Z, Liang F, Hong B, Young JC, Sussman MR, Harper JF, Sze H. *An endoplasmic reticulum-bound Ca2+/Mn2+ pump, ECA1, supports plant growth and confers tolerance to Mn2+ stress.* Plant Physiol. 2002;130(1):128–137. doi:10.1104/pp.004440. PMID 12226493 (paralog ECA1, context). [a]
6. He J, Rössner N, Hoang MTT, Alejandro S, Peiter E. *Transport, functions, and interaction of calcium and manganese in plant organellar compartments.* Plant Physiol. 2021;187(4):1940–1972. doi:10.1093/plphys/kiab122 (review; explicitly notes the Golgi-vs-PVC localization conflict). [b]
7. Pittman JK et al. 1999 — original ECA2/ECA3 cloning and expression analysis (sequence record AJ132388), as cited by papers 1, 2 and 6. [a]

## 3. Sequence & Domains

- Canonical sequence: 998 aa, UniProt Q9SY55 (FASTA in `reports/ECA3_Q9SY55.fasta`). [b]
- Family: **P2A-type (type IIA) P-type ATPase** — E1–E2 ion pump, active at resting cytosolic Ca2+ (no calmodulin autoinhibitory domain, unlike plant P2B/ACA pumps). TCDB superfamily 3.A.3 (P-type ATPases); P2A Ca2+-ATPase family 3.A.3.2. [b]
- InterPro annotation of Q9SY55: 36 member-database signatures, 15 integrated entries — Pfam (5), CATH-Gene3D (4), SUPERFAMILY (4), SFLD (3), NCBIfam (2), PRINTS (2), CDD, PANTHER, PROSITE (1, ATPASE_E1_E2-type), SMART (Cation_ATPase_N, SM00831-type). [c]
- GO terms (UniProt): GO:0005388 P-type calcium transporter activity; GO:0006816 calcium ion transport; GO:0005524 ATP binding; GO:0016887 ATP hydrolysis activity; GO:0000166 nucleotide binding; GO:0016020 membrane. [b]
- Topology: multi-pass membrane protein with ~10 transmembrane helices and a large cytoplasmic headpiece (A, P, N domains) — family-typical P-type ATPase architecture. [c]
- Targeting: no signal peptide and no plastid/mitochondrial transit peptide expected; membrane-anchored endomembrane pump (not organelle-targeted to plastids). [c]
- Gene structure: ECA3 is unique among Arabidopsis ECAs — 33 introns, several sharing positions with the human SERCA1 gene (as reported by Pittman et al. 1999, reiterated in Barabasz et al. 2011). [b]

## 4. Orthologs & Evolution

- **Paralogs in Arabidopsis (in-paralogs):** ECA1 (AT1G07810, UniProt P92939, ER-localized), ECA2 (AT4G00900, O23087), ECA4 (AT1G07670, Q9XES1). [b]
- ECA3 forms a **unique subbranch** of the ECA family: phylogenetic analyses (Li et al. 2008; Mills et al. 2008) show AtECA3 and OsECA3 share ~53% identity with mammalian SERCA1a — higher than with other plant ECAs (~44.6–45.1%) — i.e. plant ECA3-like proteins are structurally closest to animal SERCA pumps, not to SPCA/PMR1-type pumps. [a]
- **Cross-species orthologs:** a single ECA3-like gene in rice, OsECA3 (Os03g52090, GenBank ABF98693), suggesting the ECA3-type pump is **single-copy and functionally conserved across flowering plants** (angiosperms; divergence of Arabidopsis and rice ~150–200 Mya). ECA3-like sequences also reported in tomato. [a]/[d]
- Broader context: animals use SERCA (ER), PMCA (plasma membrane) and SPCA (Golgi); plants lack SPCA-type pumps and instead use the ECA/P2A family in the secretory pathway — ECA3 is the plant functional counterpart of Golgi/secretory-pathway Ca2+/Mn2+ pumping. [d]

## 5. Expression

- ECA3 is **expressed in all major organs** of Arabidopsis (Pittman et al. 1999; reiterated in Barabasz et al. 2011). [a]
- Quantitative expression resources for AT1G10130 exist (clade-appropriate routing): BAR Arabidopsis eFP Browser / AtGenExpress compendia, Genevestigator, ATTED-II co-expression, Expression Atlas (plants.ensembl.org). Per-tissue numerical values were not retrieved in this run; qualitative literature statement above is the verified finding. [b]

## 6. Structure

- **No experimental structure** exists for ECA3 or any plant P2A ATPase (InterPro structure counter for Q9SY55 = 0). Recorded as an absence-of-data finding. [b]
- **AlphaFold DB model AF-Q9SY55-F1 is available** (UniProt record flagged `in_alphafold: true`); per-residue pLDDT confidence is stored in the model. Numerical pLDDT values were not retrievable in this run (API blocked); typical P-type ATPase AlphaFold models are high-confidence in the transmembrane and headpiece domains with lower confidence in flexible loops. [c]
- **Homolog experimental structures** (extrapolation): rabbit SERCA1a structures, e.g. PDB 1SU4 (2.6 Å, two Ca2+ bound, 10 TM helices), plus 3W5B, 3B9R, 3N5K, 3N8G, 3TLM — multiple conformational states (E1/E2) of the pump cycle. [d]

## 7. Function & Interactions

- **Molecular function:** ATP-driven P-type pump translocating **Ca2+ and Mn2+** from the cytosol into endomembrane (Golgi/post-Golgi) compartments. [a] — demonstrated by functional complementation of yeast strain K616 (pmr1 pmc1 cnb1, lacking Golgi and vacuolar Ca2+ pumps): AtECA3 restored growth on Ca2+-depleted medium and conferred tolerance to toxic Mn2+ (1 mM). [a] (Li et al. 2008)
- **Ion specificity:** crucial for Mn nutrition; **not** involved in Cu, Fe or Zn transport in Arabidopsis (Mills et al. 2008). Note: heterologous tobacco data suggested possible Zn effects (Barabasz et al. 2011) — see Open Questions. [a]
- **Subcellular localization (conflicted, see §9):** Golgi / post-Golgi / endosome-PVC / trans-Golgi network (TGN) — competing reports. [a]
- **Protein–protein interactions:** no experimentally verified PPIs for Q9SY55 were retrieved from STRING/BioGRID in this run — recorded as a **data gap, not as absence of interactions**. [b]
- **Functional/genetic network in Mn homeostasis:** ECA3 acts together with NRAMP1/NRAMP2 (vacuolar Mn mobilization), MTP11 (cis-Golgi Mn exporter), MTP8 (vacuolar sequestration) and CCX transporters; severe Mn-deficiency phenotypes in `eca3 nramp1 nramp2` triple mutants (Farthing et al. 2023, PMID 37228331). [a]

## 8. Phenotype (plant — TAIR/mutant resources; no human disease relevance applies)

- `eca3` T-DNA knockout mutants (multiple independent alleles): under **Mn-deficient** conditions become chlorotic with strongly inhibited root and shoot growth after ~8–9 d; phenotype **rescued by Mn supplementation** → ECA3 is required for Mn nutrition. Not hypersensitive to low Ca2+ or Zn deficiency. [a] (Mills et al. 2008)
- `eca3` mutants show **severely reduced Ca2+-stimulated root growth** (3 mM Ca2+), a phenotype not rescued by ER-localized ECA1; root growth sensitive to 50 µM Mn2+ (Mn detoxification role); mutant roots secrete ~65% more apoplastic protein (peroxidase activity), indicating altered secretory processes. [a] (Li et al. 2008)
- **Overexpression in tobacco (35S::AtECA3):** improved growth/Mn-efficiency at moderate Mn (2 µM), increased tolerance to toxic Mn (100 µM), slight tolerance to Ca deficiency. [a] (Barabasz et al. 2011)
- Mutant seed/stock lines: multiple independent T-DNA insertion alleles were isolated and used by Mills et al. (2008) and Li et al. (2008); line-level SALK IDs were not retrieved in this run (available via TAIR/SIGnAL for AT1G10130). [b]

## 9. Open Questions & Controversies

1. **Exact subcellular compartment is contested:** Mills et al. 2008 report Golgi localization; Li et al. 2008 report a subpopulation of endosomes/prevacuolar compartments (partial colocalization with Ara7); Farthing et al. 2023 report trans-Golgi/TGN (with MTP11 at cis-Golgi). He et al. 2021 (review) explicitly note this discrepancy. Current consensus leans toward Golgi/TGN–endosomal compartments of the secretory pathway rather than a single organelle. [a]
2. **Relative contributions to Mn homeostasis:** ECA3 vs group 8/9 CDFs (MTP8/MTP11) vs NRAMPs — partially resolved by Farthing et al. 2023 (`eca3 nramp1 nramp2` synthetic phenotypes), but quantitative partitioning remains open. [a]
3. **Zn transport:** Mills et al. 2008 found no Zn-deficiency phenotype in `eca3`; Barabasz et al. 2011 suggested Zn effects in tobacco overexpression. Unresolved whether Zn is a direct substrate. [a]
4. **997 vs 998 aa:** cloned Ler cDNA (AJ132388) encodes 997 residues and differs from the Col-0 reference in 4 bp (Mills et al. 2008); UniProt canonical (Col-0) is 998 aa. Minor, but flagged. [a]/[b]
5. **No experimental structure:** mechanistic cycle (E1/E2 conformations) for plant P2A pumps is inferred from SERCA structures only. [d]
6. **Regulation:** P2A pumps are active at resting Ca2+ and lack the calmodulin autoinhibition of P2B/ACA pumps; how ECA3 is regulated in planta (e.g. by Ca2+ sensors CBL/CIPK acting on partner transporters) is an active research area. [b]

## 10. Evidence Table

| Claim | Tier | Source |
|---|---|---|
| Identity: ECA3 = AT1G10130 = Q9SY55, taxon 3702 | [b] | UniProt, TAIR, NCBI Gene 837550, Ensembl Plants |
| 998 aa P2A-type ATPase, GO:0005388/0006816 | [b]/[c] | UniProt, InterPro API |
| Ca2+/Mn2+ pump activity into endomembranes (yeast K616 complementation) | [a] | Li et al. 2008 (PMC2492598) |
| Crucial role in Mn nutrition; eca3 chlorotic under −Mn, rescued by +Mn | [a] | Mills et al. 2008 (PMC2230566) |
| Reduced Ca2+-stimulated root growth; Mn-detox role; altered secretion | [a] | Li et al. 2008 (PMC2492598) |
| Localization: Golgi vs endosome/PVC vs TGN (conflict) | [a] | Mills 2008; Li 2008; Farthing 2023 (PMID 37228331); He 2021 review |
| Expressed in all major organs | [a] | Pittman et al. 1999; Barabasz et al. 2011 |
| Tobacco 35S::ECA3 improves Mn efficiency/tolerance | [a] | Barabasz et al. 2011, Environ Exp Bot 72:202–209 |
| ECA3 subbranch closest to animal SERCA (~53% identity to SERCA1a) | [a] | Li et al. 2008, Mills et al. 2008 phylogenies |
| Single ECA3-like ortholog in rice (Os03g52090); conserved in angiosperms | [a]/[d] | Li et al. 2008 |
| Paralogs ECA1/2/4 (P92939, O23087, Q9XES1) | [b] | UniProt |
| No experimental structure for ECA3 | [b] | InterPro (structures=0); PDB |
| AlphaFold model AF-Q9SY55-F1 exists | [c] | AlphaFold DB / UniProt flag |
| SERCA1a experimental structures (1SU4 etc.) as mechanistic template | [d] | RCSB PDB |
| ~10 TM helices, A/P/N headpiece, no signal/transit peptide | [c] | P-type ATPase family architecture, computational |
| No verified PPIs for Q9SY55 retrieved (data gap) | [b] | STRING/BioGRID query this run |

## 11. Sources

- UniProtKB Q9SY55 (ECA3_ARATH) — https://www.uniprot.org/uniprotkb/Q9SY55
- InterPro entry for Q9SY55 — https://www.ebi.ac.uk/interpro/ (API: /interpro/api/protein/UniProt/Q9SY55/)
- TAIR locus AT1G10130 — https://www.arabidopsis.org/servlets/TairObject?name=AT1G10130
- NCBI Gene 837550; GenBank EU082212, AJ132388 — https://www.ncbi.nlm.nih.gov/
- Ensembl Plants, gene AT1G10130 — http://plants.ensembl.org/Arabidopsis_thaliana/Gene/Summary?g=AT1G10130
- AlphaFold DB model AF-Q9SY55-F1 — https://alphafold.ebi.ac.uk/
- TCDB P-type ATPase superfamily 3.A.3 — https://tcdb.org/
- Publications: PMC2230566 (PMID 18024560, doi:10.1104/pp.107.110817); PMC2492598 (PMID 18567829, doi:10.1104/pp.108.119909); PMID 12226493 (doi:10.1104/pp.004440, ECA1); Barabasz et al. 2011, Environ Exp Bot 72:202–209; PMID 37228331; doi:10.1093/plphys/kiab122 (He et al. 2021 review)
- RCSB PDB: 1SU4, 3W5B, 3B9R, 3N5K, 3N8G, 3TLM (SERCA1a) — https://www.rcsb.org/
- Expression resources: BAR eFP Browser / AtGenExpress (bar.utoronto.ca), Genevestigator, Expression Atlas
