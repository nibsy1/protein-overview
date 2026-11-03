# Mandatory critic agent (adversarial refutation)

## Summary
Critic agent that tries to refute each hypothesis using only stored evidence; only surviving hypotheses reach the report, with confidence scores.

## Details
- Must attempt refutation per hypothesis (contradicting evidence, tier weaknesses, alternative explanations).
- Verdicts written to store; nothing reported as fact without passing the critic.

## Acceptance criteria
- Critic verdicts recorded for every ECA3 hypothesis; at least one hypothesis demoted or refuted by stored evidence in the reference run.

Ref: PRD §3
