# FRICTIONAL.md - Which One Is Right? Scoring Taggers Against a Gold Set

**Fellow:** Satwik Reddy Sripathi
**Folder:** `2026-08-23-personalized-roadmap-goldenset`
**Date:** Aug 23, 2026 (week ending August 24, 2026)
**Type:** Project update
**Project:** Personalized, Project-Driven Reading Roadmaps (CaNCURE)

> An append-only log of the process behind this week's work: what I set out to do, where it resisted, what
> I decided, and what Claude contributed as an assistant. Not a performance review; a record of the real work.

## What I set out to do and why

Built a gold standard so tagger quality could be judged against truth, not just against each other.

## What I did (my contribution)

- Designed the gold-set protocol (sample prioritising materials and disagreements; precision/recall/F1 vs faculty truth).
- Decided which fields faculty should judge vs which I could author-grade, and required blind grading to avoid bias.
- Built the two-annotator workflow (Cohen's kappa + adjudication) for credibility.

## Where it resisted, and what I decided

- I realised a tagger-vs-tagger comparison cannot declare a quality winner; I added the gold-vs-truth scoring to fix that.
- Designing blind grading so my own grading stayed honest took care.

## What Claude contributed (assistant)

- Implemented the gold-review builder, the blind-mode split, and the scoring script to my spec.
- Generated the evidence-location aid.

Claude acted as an implementation assistant under my direction. The research questions, the framing, the
design decisions, the interpretation of results, the faculty collaboration, and the final acceptance of
every output were mine.

## Accepted / changed / rejected

I accepted author-grading only for objective fields and only blind; faculty review reserved for genuine judgment.
