# Benchmark harness + end-to-end validation

## Summary
Scoring harness against `benchmarks/benchmark-panel.md` and the ECA3 reference run.

## Details
- Metrics per benchmark protein: hypothesis recall vs gold annotations, precision (zero fabricated claims — hard fail), per-section completeness, discriminability (each hypothesis has ≥1 distinguishing experiment).
- Reference case: ECA3 (AT1G10130/Q9SY55, with OsECA3 multi-candidate comparison).

## Acceptance criteria
- Harness scores all 12 benchmark proteins; ECA3 end-to-end run passes integrity checks and recall targets.

Ref: PRD §8, §9
