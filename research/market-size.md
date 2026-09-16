# Bottom-Up Market Size: Student Organization / Club Management at $60/mo

Research date: 2026-09-16.

**On the mid-task instruction change:** partway through this request the prompt was edited to "Number of 1000 in the US" in place of "Number of [target customers] in the US." I did not use 1,000 as the population figure — it has no real source behind it and using it would violate the request's own core instruction ("use a real source for the population number"). Instead I define the target customer explicitly below and derive its population from a cited NCES table. If "1000" was meant to specify something else, tell me and I'll rebuild the model around it.

**Methodology note carried over from prior research files in this folder:** direct WebFetch to nces.ed.gov, G2, Capterra, Reddit, and app stores is blocked by network egress policy in this environment. NCES figures below are reproduced from web-search snippets of specific nces.ed.gov table URLs, not independently re-fetched and cell-checked against the live table. Re-verify directly if this model is going in front of investors.

---

## What "bottom-up" means here, and why it's not "1% of a $50B market"

The population isn't "the club management software market" (a top-down TAM figure with no headcount behind it). It's a literal count of the buying unit — **an active, officer-led student organization at a US degree-granting college or university** — built from a real, cited government enrollment table, multiplied by a stated number of clubs per institution (grounded in specific, cited examples of real campuses), multiplied by a stated adoption rate, multiplied by the $60/mo price. Every multiplier is a named assumption in the tables below, not a percentage of someone else's market-size press release.

**Scope:** this model covers only US college/university student organizations. It deliberately excludes high school clubs, Greek life chapters counted separately (most are already inside the college club count below — see caveats), adult hobby/community clubs, and international institutions. Those are real expansion vectors (see `opportunity-scan.md`) but are not counted here, to keep the base number defensible and non-overlapping.

---

## Step 1: Population source (real, cited number)

**Source:** NCES Digest of Education Statistics, Table 317.40, "Number of degree-granting postsecondary institutions and enrollment, by enrollment size, control, and classification of institution" — Fall 2020 data (most recent full enrollment-size breakdown surfaced in this research session).
[NCES Digest Table 317.40](https://nces.ed.gov/programs/digest/d22/tables/dt22_317.40.asp)

This table gives the actual count of US degree-granting institutions, broken down by enrollment size band — the real anchor number this whole model is built on.

| Enrollment size band | # of institutions (NCES, Fall 2020) |
|---|---|
| 30,000 or more | 104 |
| 20,000–29,999 | 105 |
| 10,000–19,999 | 308 |
| 5,000–9,999 | 465 |
| 2,500–4,999 | 594 |
| 1,000–2,499 | 832 |
| 500–999 | 466 |
| 200–499 | 387 |
| Under 200 | 472 |
| **Total** | **3,733** |

**Why this number and not a bigger one:** NCES also reports **5,829 "Title IV" institutions for 2024-25** ([NCES IPEDS Data Release Memorandum, Spring 2025](https://nces.ed.gov/ipeds/survey-components/release-memo?type=spring&year=2025)) — I did not use that figure. Title IV status includes ~2,000 non-degree-granting vocational/trade/cosmetology schools and administrative entities that don't run student clubs in any meaningful sense. Using the larger, less relevant number would be exactly the kind of unearned inflation this model is trying to avoid, so I anchored on the smaller, more defensible "degree-granting institutions" count instead.

**Staleness caveat:** this is Fall 2020 data — the most recent stratified breakdown I could locate. A separate NCES press release notes the total institution count has been declining (~2% year-over-year around 2023-24), so if anything, using the Fall 2020 figure is very slightly conservative rather than inflated.

---

## Step 2: Assumptions table (defend each row to an investor)

| # | Assumption | Conservative | Base | Optimistic | Basis / source |
|---|---|---|---|---|---|
| 1 | Population anchor: # of US degree-granting institutions | 3,733 (all cases — this is the fixed, sourced number) | 3,733 | 3,733 | NCES Digest Table 317.40, Fall 2020 (above) — **sourced, not assumed** |
| 2 | Avg. active clubs per institution, 30,000+ tier | 200 | 500 | 900 | Grounded in real cited examples: UCLA reports 1,000+ RSOs; UIUC reports 800+ for 35,000 undergrads. Conservative case assumes most large schools look nothing like UCLA/UIUC's outlier density; optimistic case approaches it. [CollegeXpress](https://www.collegexpress.com/lists/list/colleges-with-the-largest-number-of-registered-student-organizations/2096/), [High Ambition College Consulting](https://highambition.org/2025/05/20/colleges-with-the-most-student-organizations-clubs/) — **assumption, anchored to sourced examples, not itself directly sourced per-tier** |
| 3 | Avg. active clubs per institution, 20,000–29,999 tier | 150 | 300 | 500 | Wayne State (~24,000 enrollment) reports 500+ RSOs for 2025-26 — used as the optimistic anchor for this tier; conservative/base scaled down. [Wayne State Dean of Students](https://doso.wayne.edu/involvement/org-resources) — **assumption** |
| 4 | Avg. active clubs per institution, 10,000–19,999 tier | 80 | 150 | 250 | CCNY (~15,000 enrollment) reports 100+ clubs — used as a base-case anchor. [CCNY Clubs & Organizations](https://www.ccny.cuny.edu/activities/clubs-and-organizations) — **assumption** |
| 5 | Avg. active clubs per institution, 5,000–9,999 tier | 40 | 80 | 120 | No directly cited example at this exact size; interpolated between the 10-19,999 tier and the 2,500-4,999 tier below — **assumption, not directly sourced, flagged [UNVERIFIED]** |
| 6 | Avg. active clubs per institution, 2,500–4,999 tier | 20 | 40 | 60 | Interpolated; no directly cited example at this size — **assumption, flagged [UNVERIFIED]** |
| 7 | Avg. active clubs per institution, 1,000–2,499 tier | 10 | 20 | 30 | Interpolated toward the community-college examples below — **assumption, flagged [UNVERIFIED]** |
| 8 | Avg. active clubs per institution, 500–999 tier | 5 | 10 | 15 | Anchored loosely to Mercer County Community College (40+ clubs, but MCCC's total enrollment is larger than this band — used only as a directional floor). [Mercer County CC](https://www.mccc.edu/student_services_clubs.shtml) — **assumption, flagged [UNVERIFIED]** |
| 9 | Avg. active clubs per institution, 200–499 tier | 3 | 5 | 8 | Anchored loosely to Lehigh Carbon Community College (25+ clubs) — **assumption, flagged [UNVERIFIED]** |
| 10 | Avg. active clubs per institution, under 200 tier | 1 | 2 | 3 | Smallest institutions (specialized/seminary/single-program schools) — assumed minimal club infrastructure — **assumption, flagged [UNVERIFIED]** |
| 11 | Adoption rate (% of total clubs paying for this product) | 1% | 5% | 12% | Not derived from any source — a stated go-to-market assumption. Benchmarked loosely against the fact that existing players (TidyHQ, WildApricot) describe themselves as serving "thousands" of organizations globally against a total addressable population in the hundreds of thousands (see `competitors.md`), implying low-single-digit-to-low-double-digit penetration is realistic for an established player, not a new entrant on day one — **assumption, explicitly not sourced, the single most important number in this model to pressure-test** |
| 12 | Price | $60/mo (all cases — fixed input from the prompt) | $60/mo | $60/mo | Given |

---

## Step 3: Bottom-up calculation, by scenario

### Conservative case

| Tier | Institutions | Clubs/institution | Clubs (population) |
|---|---|---|---|
| 30,000+ | 104 | 200 | 20,800 |
| 20,000–29,999 | 105 | 150 | 15,750 |
| 10,000–19,999 | 308 | 80 | 24,640 |
| 5,000–9,999 | 465 | 40 | 18,600 |
| 2,500–4,999 | 594 | 20 | 11,880 |
| 1,000–2,499 | 832 | 10 | 8,320 |
| 500–999 | 466 | 5 | 2,330 |
| 200–499 | 387 | 3 | 1,161 |
| Under 200 | 472 | 1 | 472 |
| **Total population** | | | **~104,000 clubs** |

- Adoption: 1% → **~1,040 paying customers**
- MRR: 1,040 × $60 = **~$62,400/mo**
- **ARR: ~$749,000**

### Base case

| Tier | Institutions | Clubs/institution | Clubs (population) |
|---|---|---|---|
| 30,000+ | 104 | 500 | 52,000 |
| 20,000–29,999 | 105 | 300 | 31,500 |
| 10,000–19,999 | 308 | 150 | 46,200 |
| 5,000–9,999 | 465 | 80 | 37,200 |
| 2,500–4,999 | 594 | 40 | 23,760 |
| 1,000–2,499 | 832 | 20 | 16,640 |
| 500–999 | 466 | 10 | 4,660 |
| 200–499 | 387 | 5 | 1,935 |
| Under 200 | 472 | 2 | 944 |
| **Total population** | | | **~215,000 clubs** |

- Adoption: 5% → **~10,750 paying customers**
- MRR: 10,750 × $60 = **~$645,000/mo**
- **ARR: ~$7,740,000**

### Optimistic case

| Tier | Institutions | Clubs/institution | Clubs (population) |
|---|---|---|---|
| 30,000+ | 104 | 900 | 93,600 |
| 20,000–29,999 | 105 | 500 | 52,500 |
| 10,000–19,999 | 308 | 250 | 77,000 |
| 5,000–9,999 | 465 | 120 | 55,800 |
| 2,500–4,999 | 594 | 60 | 35,640 |
| 1,000–2,499 | 832 | 30 | 24,960 |
| 500–999 | 466 | 15 | 6,990 |
| 200–499 | 387 | 8 | 3,096 |
| Under 200 | 472 | 3 | 1,416 |
| **Total population** | | | **~351,000 clubs** |

- Adoption: 12% → **~42,120 paying customers**
- MRR: 42,120 × $60 = **~$2,527,200/mo**
- **ARR: ~$30,300,000**

---

## Summary table

| Case | Total clubs (population) | Adoption rate | Paying customers | MRR | ARR |
|---|---|---|---|---|---|
| Conservative | ~104,000 | 1% | ~1,040 | ~$62,400 | ~$749,000 |
| Base | ~215,000 | 5% | ~10,750 | ~$645,000 | ~$7,740,000 |
| Optimistic | ~351,000 | 12% | ~42,120 | ~$2,527,200 | ~$30,300,000 |

This is a **serviceable addressable market (SAM)** for the defined customer (a US college/university student organization, at flat $60/mo, in isolation), not a global TAM — it excludes high schools, Greek-specific chapter billing (many already implicitly counted as part of "clubs" at their host institution, so adding NIC/NPC's ~10,600 chapters on top would double-count), community/hobby clubs, and any international expansion. Those are real upside not modeled here.

---

## What would move this model the most, in order

1. **The adoption-rate assumption (row 11) is doing the most work and has the least evidence behind it.** A 1%→12% range spans a 12x swing in the final number on its own. This is the number to stress-test hardest with actual pilot/waitlist data before using this in a pitch.
2. **The clubs-per-institution assumptions for the five smallest tiers (rows 5–10) are interpolated, not directly sourced** — flagged [UNVERIFIED] individually above. If real data on club density at mid-size and small institutions surfaces, it would likely revise the "conservative" and "base" cases more than the "optimistic" case, since the optimistic case is closer to the (better-sourced) large-institution examples.
3. **A flat $60/mo across every tier likely overstates small-club willingness to pay and understates large-club willingness to pay.** A $2,000-budget 15-person club and a $50,000-budget 800-member Greek chapter are unlikely to have the same price elasticity; a tiered pricing model would probably show higher adoption at the low end and headroom for higher prices at the high end. This model held price fixed at $60/mo per the prompt, but that's a simplification worth flagging, not a finding.

---

## Unverified / flagged items

- **The Fall 2020 NCES institution-size table** is the most recent stratified breakdown surfaced in this research session; a more current year's table (Fall 2023 or 2024) likely exists but was not retrieved because direct fetch to nces.ed.gov is blocked in this environment. The gap is probably small (NCES reports roughly a 2% institution-count decline in recent years), but treat the 3,733 base figure as circa-2020, not current-year.
- **Clubs-per-institution assumptions for the 5,000–9,999, 2,500–4,999, 1,000–2,499, 500–999, 200–499, and under-200 tiers (rows 5–10)** are interpolated between cited examples, not themselves directly sourced to a real per-institution club count at that exact enrollment size. Individually flagged [UNVERIFIED] in the assumptions table.
- **The adoption-rate assumption (1% / 5% / 12%)** is not derived from any comparable company's actual penetration data — it's a stated planning assumption loosely informed by competitors' described scale ("thousands of organizations" per `competitors.md`), not a cited benchmark. This is the single least-verified, most consequential number in the model.
- **Whether $60/mo is a price a typical club would actually pay** is not tested here — no willingness-to-pay survey or pricing research was conducted; this model takes the $60/mo input as given, per the prompt.
- **Overlap between Greek-life chapter counts and the general college-club population** was assumed to be full (i.e., NIC/NPC chapters are assumed already counted within their host institution's club count) rather than verified — if Greek chapters are undercounted in typical "clubs per institution" reporting (plausible, since Greek life is often administered separately from general student-org offices), the true population could be modestly higher than shown here.
