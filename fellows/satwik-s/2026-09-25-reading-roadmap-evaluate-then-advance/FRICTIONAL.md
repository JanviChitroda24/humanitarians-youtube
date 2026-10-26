# FRICTIONAL.md - Evaluate, Then Advance

**Fellow:** Satwik Reddy Sripathi
**Folder:** `2026-09-25-reading-roadmap-evaluate-then-advance`
**Date:** Sep 25, 2026 (week ending September 25, 2026)
**Type:** Project update
**Project:** Personalized, Project-Driven Reading Roadmaps (CaNCURE)

> An append-only log of the process behind this week's work: what I set out to do, where it resisted, what
> I decided, and what Claude contributed as an assistant. Not a performance review; a record of the real work.

## What I set out to do and why

Ran the full evaluation pipeline: the MCQ gate with item pools and prune-after-evaluate.

## What I did (my contribution)

- Specified the end-to-end evaluation pipeline and the gate semantics (advance / hold / remediate).
- Defined item pools with deterministic per-student sampling and the open-ended grading seam.
- Set the reporting so the gate's decisions are inspectable.

## Where it resisted, and what I decided

- Deciding how the gate reports a gap (remediate-to the specific missing prerequisite) took design.
- Keeping the open-ended path honest (defer to a judge rather than fake-grade) mattered.

## What Claude contributed (assistant)

- Implemented the evaluation engine and the CSV artifacts to my spec.
- Produced the readable trace and example run.

Claude acted as an implementation assistant under my direction. The research questions, the framing, the
design decisions, the interpretation of results, the faculty collaboration, and the final acceptance of
every output were mine.

## Accepted / changed / rejected

I accepted the defer-by-default open grader; I rejected pretending to grade free text offline.
