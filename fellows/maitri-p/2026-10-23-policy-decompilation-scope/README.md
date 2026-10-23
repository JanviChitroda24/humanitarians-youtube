# Can a Model's Choices Become Rules?

**Type:** Weekly update (research and scope)
**Fellow:** Maitri P. · **Voice:** Kokoro `af_bella` (Bella), a synthetic narrator — disclosed on the outro card.

## This week's contribution
**Question:** can a small trained model's choices be expressed as simple, readable rules — and how closely would those rules match the model?
**What I did:** started a new research task, Policy Decompilation, connected to Optimus's reasoning work; reviewed the problem and discussed the wider goal with Dev; looked at ways to compare model and rules — same actions, performance, and rule complexity.
**Clarified:** explaining a model's behaviour and improving its reasoning are separate questions.
**Observed:** no model trained and no experiment run yet; success criteria and timeline still to be settled.
**Next experiment:** set up a small reproducible baseline, likely CartPole, and start collecting decisions to test rule extraction.

## Human and AI work
**My decisions and verification:** the topic and brief; reviewed the cuts.
**AI tools and what they generated:** Claude Code (Anthropic) wrote the beat sheet from my brief, built the custom scenes in `scenes/` and rendered. Kokoro produced the narration.
**What I rejected or corrected:** see `FRICTIONAL.md`.
**What remains unverified:** see `FACTCHECK.md`.

## Reproduce
- **Brutalist toolkit:** commit `6fc9987` **plus local uncommitted changes** (scenes in `scenes/`, Windows fixes). Not yet upstream.
- **Beat sheets:** `beat_sheet.json` (16:9), `vertical/beat_sheet.json` (9:16 native layouts).
- **Checks:** `FACTCHECK.md`, `SHOTLIST.md`, `PROMPTS.md`. GATE V: 0 blockers on both aspects.

## Watch and review
- **Landscape** — `PolicyDecompilation_MaitriP.mp4` — 3840×2160 — 1:23.8 — SHA-256 `e49aff6a6eabc034f2a85376a1bbf8a340ebd23e061a9cde7a8b51fa87ac71bb`
  Drive: pending
- **Vertical** — `PolicyDecompilation-vertical.mp4` — 2160×3840 — 1:23.8 — SHA-256 `a770b43bf7e5c080cecc1f357613e0db7be8e275e580173a3440d081c5b77f46`
  Drive: pending
