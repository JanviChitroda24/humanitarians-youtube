# FRICTIONAL.md - Does It Reason, or Just Retrieve?

**Fellow:** Satwik Reddy Sripathi
**Folder:** `2026-08-29-reading-roadmap-reason-or-retreive`
**Date:** Aug 29, 2026 (week ending August 29, 2026)
**Type:** Project update
**Project:** Personalized, Project-Driven Reading Roadmaps (CaNCURE)

> An append-only log of the process behind this week's work: what I set out to do, where it resisted, what
> I decided, and what Claude contributed as an assistant. Not a performance review; a record of the real work.

## What I set out to do and why

Defended the core contribution: the graph constraint, not similarity, is what makes this reasoning.

## What I did (my contribution)

- Articulated and demonstrated the reordering-not-retrieval contribution with the exclusion log as evidence.
- Used two dissimilar projects (LNP-siRNA vs photothermal) to show genuine personalization (Jaccard divergence).
- Framed the exclusion of high-similarity-but-off-scope sections as a feature that proves selection over retrieval.

## Where it resisted, and what I decided

- Keeping the demo from reading as top-k search required foregrounding the dependency ordering and the exclusions.
- Tuning the selection levers so two projects diverge meaningfully took iteration.

## What Claude contributed (assistant)

- Produced the two demo roadmaps and the exclusion analysis from my design.
- Drafted the comparison visuals.

Claude acted as an implementation assistant under my direction. The research questions, the framing, the
design decisions, the interpretation of results, the faculty collaboration, and the final acceptance of
every output were mine.

## Accepted / changed / rejected

I accepted the exclusion log as core evidence; I rejected framings that reduced the system to retrieval.
