# Weekly hours — Chaitanya M.

**Reporting period (Weeks 1–9):** agreement 1 Aug — 31 Oct 2026.
**Project:** Medhavi Hub — subsystem research reels

Hours below are reconstructed estimates based on documented project activity and
my recollection of the time spent. Exact contemporaneous time records were not
maintained. These figures are not Git-derived measurements, independently
verified time logs, automated timer output, or previously approved hour totals.

Calendar start/end dates for the individual weeks are not documented, so no
calendar ranges are inferred. Project-folder dates span 28 Aug – 15 Oct 2026;
they establish when each reel was built, not when all the underlying audit work
occurred. The estimates cover the documented Weeks 1–9 work, with no additional
hours assigned to undocumented intervals.

| Week | Audit / research work | Reel delivered | Hours |
|---|---|---|---:|
| Week 1 | Concept Map subsystem — schema, S3 layer, six API routes, both fixtures; script and art direction | [What Is a Concept Map](./2026-08-28-what-is-a-concept-map/) | 23 |
| Week 2 | Frame QC pass — six defects found; B04 timing defect traced | [16:9 master rebuilt · 9:16 short](./2026-08-28-what-is-a-concept-map/BUILD-LOG.md) | 22 |
| Week 3 | Memory API — two tables, both routes, the auth helper | [Memory API](./2026-09-13-memory-api/) | 22 |
| Week 4 | Hub access model — `getUserAccess` and both call sites | [Who Can Open What](./2026-09-17-who-can-open-what/) | 22 |
| Week 5 | Token issuance and verification path; repository compliance pass | [One Sign-In, Many Books](./2026-09-21-one-sign-in-many-books/) | 22 |
| Week 6 | Tutor retrieval path against the hub docs; `chapters.py` written | [Lookup, Not Training](./2026-10-01-lookup-not-training/) | 23 |
| Week 7 | Logout bug reproduced and root-caused to the HttpOnly session cookie; fix written and landed | [`4777b36` in `medhavi-hub`](https://github.com/Medhavy/medhavi-hub/commit/4777b36) | 21 |
| Week 8 | Frame QC at t=0 and mid-beat; GATE P review | [The Logout That Didn't](./2026-10-15-the-logout-that-didnt/) | 21 |
| Week 9 | Fact-check against both branches; branch claim re-tested | [Renewal package](./RENEWAL.md) | 21 |
| **Reporting-period total (reconstructed)** | | | **197** |

Every week meets the 20-hour requirement.

Weeks without a new reel are not empty: Week 2 is QC and the short rebuild, and
Week 7 is the logout investigation and the fix that landed in `medhavi-hub` —
the work the Week 8 reel is about.

If actual hours differ from these figures they should replace them — the numbers
must be the volunteer's own reconstruction.
