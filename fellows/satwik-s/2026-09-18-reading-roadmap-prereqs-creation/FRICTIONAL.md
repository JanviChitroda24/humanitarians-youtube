# FRICTIONAL.md - Read the Book, Draft the Graph

**Fellow:** Satwik Reddy Sripathi
**Folder:** `2026-09-18-reading-roadmap-prereqs-creation`
**Date:** Sep 18, 2026 (week ending September 20, 2026)
**Type:** Project update
**Project:** Personalized, Project-Driven Reading Roadmaps (CaNCURE)

> An append-only log of the process behind this week's work: what I set out to do, where it resisted, what
> I decided, and what Claude contributed as an assistant. Not a performance review; a record of the real work.

## What I set out to do and why

Built the prerequisite dependency graph from the textbook, as a reviewable draft for faculty.

## What I did (my contribution)

- Designed the two-pass build (faculty-authoritative prerequisites first, then proposed conceptual/method links) with provenance on every edge.
- Enforced the DAG safety rule (every prerequisite earlier in the book) and cycle validation as a hard gate.
- Set up the faculty-review workflow so every edge is a draft with an approve column.

## Where it resisted, and what I decided

- Prerequisite cycles had to be impossible, not just discouraged; I made the earlier-in-book rule a hard constraint.
- Keeping edges reviewable (provenance, needs_review) rather than a black box took deliberate design.

## What Claude contributed (assistant)

- Implemented the graph builder, validation, and GraphML export to my design.
- Ran the build and produced the review files.

Claude acted as an implementation assistant under my direction. The research questions, the framing, the
design decisions, the interpretation of results, the faculty collaboration, and the final acceptance of
every output were mine.

## Accepted / changed / rejected

I accepted the two-pass provenance-tracked design; I rejected any un-reviewable edge.
