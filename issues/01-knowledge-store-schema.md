# Knowledge store schema (repo-native JSON/Markdown)

## Summary
Define and implement the versioned, repo-native knowledge store that all agents read/write and from which reports are generated deterministically.

## Details
- Layout: `proteins/<canonical-id>/protein.json`, `proteins/<canonical-id>/evidence/*.md`, `proteins/<canonical-id>/hypotheses/*.md`, `proteins/<canonical-id>/decision-log.md`, plus run metadata (query URL + timestamp per fetched fact).
- Multi-candidate runs: one directory per candidate (e.g. AtECA3 and OsECA3 side by side) with a comparison entry.
- Schema must encode: claims with exactly one evidence tier ([a] experimental, [b] curated/similarity, [c] computational, [d] ortholog-extrapolated), source references, conflict flags, hypothesis ranking and critic verdicts.
- Git-diffable; no binary formats.

## Acceptance criteria
- Schema documented; a sample store for ECA3 (Q9SY55) validates against it.
- Report generator can render the fixed section order purely from store files.

Ref: docs/PRD-functional-characterization-workflow.md §4
