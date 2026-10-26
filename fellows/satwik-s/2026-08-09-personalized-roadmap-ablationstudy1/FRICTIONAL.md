# FRICTIONAL.md - Does the Fancy Part Earn It? A Tagging Ablation

**Fellow:** Satwik Reddy Sripathi
**Folder:** `2026-08-09-personalized-roadmap-ablationstudy1`
**Date:** Aug 9, 2026 (week ending August 9, 2026)
**Type:** Project update
**Project:** Personalized, Project-Driven Reading Roadmaps (CaNCURE)

> An append-only log of the process behind this week's work: what I set out to do, where it resisted, what
> I decided, and what Claude contributed as an assistant. Not a performance review; a record of the real work.

## What I set out to do and why

Tested whether the LLM tagging actually earns its place against a deterministic baseline.

## What I did (my contribution)

- Designed the ablation (deterministic rule-based tagger vs a pinned open LLM) and the metrics (field Jaccard, stability, cross-agreement).
- Chose a reproducible, self-hosted model arm over a hosted API so the methods paper stays replicable.
- Interpreted the results and framed what the ablation can and cannot conclude.

## Where it resisted, and what I decided

- The first numbers looked too good; I pushed back on them and found the stability/agreement was inflated by empty-vs-empty field matches.
- I added a non-empty-restricted metric so the headline figure was not resting on padding.

## What Claude contributed (assistant)

- Implemented the metric functions and the comparison script to my design.
- Ran the paired comparisons and tabulated outputs.

Claude acted as an implementation assistant under my direction. The research questions, the framing, the
design decisions, the interpretation of results, the faculty collaboration, and the final acceptance of
every output were mine.

## Accepted / changed / rejected

I accepted the deterministic baseline as the reproducible default; I flagged the inflated agreement as a caveat rather than reporting it as a win.
