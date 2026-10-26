# FRICTIONAL.md - Test Before You Advance

**Fellow:** Satwik Reddy Sripathi
**Folder:** `2026-09-11-reading-roadmap-test-before-building`
**Date:** Sep 11, 2026 (week ending September 11, 2026)
**Type:** Project update
**Project:** Personalized, Project-Driven Reading Roadmaps (CaNCURE)

> An append-only log of the process behind this week's work: what I set out to do, where it resisted, what
> I decided, and what Claude contributed as an assistant. Not a performance review; a record of the real work.

## What I set out to do and why

Designed the test-to-advance gate: never assume prior knowledge, evaluate first, prune on pass.

## What I did (my contribution)

- Designed the gate around prune-after-evaluate (evaluate a prerequisite before trusting it) and descend-on-fail, grounded in Knowledge Space Theory and Bayesian Knowledge Tracing.
- Specified hard (gating) vs soft (diagnostic) prerequisites and the mastery threshold.
- Grounded the design in the assessment literature for the paper.

## Where it resisted, and what I decided

- The naive 'assume the student knows the basics' approach is wrong; I made evaluate-first the core rule.
- Deciding how failure localises (descend into sub-prerequisites) took design work.

## What Claude contributed (assistant)

- Implemented the gate engine and item-pool sampling to my specification.
- Drafted the worked example.

Claude acted as an implementation assistant under my direction. The research questions, the framing, the
design decisions, the interpretation of results, the faculty collaboration, and the final acceptance of
every output were mine.

## Accepted / changed / rejected

I accepted prune-after-evaluate; I rejected pre-declared 'known' sets.
