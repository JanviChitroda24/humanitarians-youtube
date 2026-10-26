# FRICTIONAL.md - Personalized, Project-Driven Reading Roadmaps (Introduction)

**Fellow:** Satwik Reddy Sripathi
**Folder:** `2026-07-28-personalized-reading-roadmap-introduction`
**Date:** Jul 28, 2026 (week ending July 27, 2026)
**Type:** Project update
**Project:** Personalized, Project-Driven Reading Roadmaps (CaNCURE)

> An append-only log of the process behind this week's work: what I set out to do, where it resisted, what
> I decided, and what Claude contributed as an assistant. Not a performance review; a record of the real work.

## What I set out to do and why

Introduced the project and the framing that governs it: this is a reordering problem, not a retrieval problem.

## What I did (my contribution)

- Defined the research problem and the central framing (reorder a textbook by learning dependency, not top-k similarity).
- Designed the four-stage pipeline architecture (ingest -> metadata -> dependency graph -> personalized sequencing) and the reproducibility constraints for a methods paper.
- Wrote the introductory weekly report and recorded the design decisions and assumptions.

## Where it resisted, and what I decided

- I had to decide up front how to keep the system from collapsing back into semantic search; I fixed the reordering-not-retrieval framing as a hard constraint before any code.
- Settling the stage boundaries so each stage produces an inspectable, editable artifact took iteration.

## What Claude contributed (assistant)

- Scaffolded the repository skeleton and Pydantic schemas from my specification.
- Drafted the beat sheet for the video from my report.

Claude acted as an implementation assistant under my direction. The research questions, the framing, the
design decisions, the interpretation of results, the faculty collaboration, and the final acceptance of
every output were mine.

## Accepted / changed / rejected

I accepted the staged artifact design; I rejected any shortcut that would make Stage 4 a plain similarity ranker.
