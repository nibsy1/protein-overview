# PRD — Agentic Functional-Characterization Workflow ("deep research pipeline")

Status: design locked via structured design interview (grill-me session)
Extends: `skills/protein-overview` (Stages 0–4 knowledge report)

## 1. Goals
- Given any eukaryotic protein identifier (UniProt accession, gene name, protein name, PDB ID, or sequence), produce a **functional characterization**, not just a data compilation.
- Must work identically for a human enzyme, a plant transcription factor, a fungal protein, and a protist protein.
- Every claim carries a source and exactly one evidence tier: [a] experimental · [b] curated/similarity · [c] computational · [d] ortholog-extrapolated.

## 2. Primary outputs (hybrid, per design session)
1. **Ranked hypothesis report** — 3–8 falsifiable functional hypotheses, each with evidence, confidence, and discriminating tests. Human-facing document with the fixed section order of the base skill plus new sections: Expression & Regulation, Comparative Homology (vs experimental structures), Hypotheses, Proposed Experiments.
2. **Living knowledge store** — machine-updatable, repo-native representation of protein → claims → sources → hypotheses (see §4).
3. **Automated experiment proposals** — per hypothesis, 1–3 discriminating experiments (wet-lab **and** in-silico), each with method, controls, predicted outcome under this hypothesis vs the top alternative, and feasibility note.

## 3. Architecture
- **Parallel domain analysts**: resolver, then concurrent harvesters — sequence/annotations, expression & regulation, structure, orthologs/evolution, literature, phenotype. Each harvester writes into the shared store.
- **Integrator**: merges analyst outputs; flags every conflict explicitly (e.g. Golgi vs PVC localization) — conflicts are never silently resolved.
- **Hypothesis generator**: systematic combination of (1) functions of the closest characterized ortholog, (2) protein-family functional templates, and (3) mechanism-first derivation from sequence/structure. Hypotheses ranked by evidence strength and discriminability.
- **Mandatory critic agent**: adversarially attempts to refute each hypothesis using only stored evidence; only surviving hypotheses reach the report, with confidence scores. Nothing is reported as fact without passing the critic.
- **Experiment designer**: attaches discriminating wet-lab + in-silico experiments to each surviving hypothesis.

## 4. Knowledge store
- Representation: **repo-native JSON/Markdown schema** — versioned files (e.g. `proteins/<id>/protein.json`, `evidence/*.md`, `hypotheses/*.md`, `decision-log.md`), diffable in git, reviewable in PRs. The report is generated deterministically from the store.

## 5. Data access
- Curated, versioned toolset of REST APIs (UniProt, NCBI eUtils, InterPro, AlphaFold DB, Expression Atlas, clade databases: TAIR, MGI, ZFIN, FlyBase, WormBase, SGD, Ensembl Plants/Fungi/Protists, Bgee…) plus web search as fallback.
- **Response caching**: every fetched fact stored with query URL and timestamp → reproducible, auditable runs.
- Polite rate-limit handling; on unreachable/empty source: retry → alternative source → only then record "absence of data" as a finding.

## 6. Standard data packages per domain
- **Expression & regulation** (plant template, clade-routed equivalents for animals/fungi): (1) developmental/tissue atlas, (2) stress & hormone compendia, (3) single-cell resolution where available, plus promoter cis-elements, TF binding/ChIP data, co-expression networks.
- **Comparative homology**: for top homologs with experimental structures (e.g. SERCA1a for ECA3) — structural superposition of the AlphaFold model onto PDB structures, mapping of conserved catalytic residues (P-site, ATP-binding, ion-binding), function-transfer table with evolutionary distance, phylogenetic placement. Labeled [d] unless tested in the organism.

## 7. Failure & ambiguity handling
- Resolver emits a **candidate set**, not a single pick: proceed with **all plausible candidates** (e.g. "ECA3" → Arabidopsis ECA3 *and* rice OsECA3, compared side by side). Every decision logged in `decision-log.md` — never silently guess.
- Hard stops only for: prokaryotic/viral input (out of scope), or zero resolvable canonical identifier.
- Low-evidence sections are marked low-confidence, not padded with family-level filler.

## 8. Evaluation
- **Benchmark panel** (`benchmarks/benchmark-panel.md`): fixed set of ~12 proteins across clades with gold-standard literature annotations; score hypothesis recall, precision (no fabricated claims), and per-section completeness.
- **Automated integrity checks on every run**: every claim has a source and exactly one tier; every citation resolves; all conflicts flagged.

## 9. Build plan (locked)
1. **Benchmark panel first** — define benchmark + gold annotations before any agent code.
2. **Full workflow at once** — store schema + all agents (resolver, harvesters, integrator, generator, critic, experiment designer) + report generator built in one pass, then validated end-to-end against the benchmark panel including ECA3 as reference case.

## 10. Non-goals
- No human disease attribution for non-human proteins; clade-appropriate routing only.
- No public exposure of any sandbox resource; loopback-only services.
- No wet-lab execution — the workflow designs experiments, humans run them.
