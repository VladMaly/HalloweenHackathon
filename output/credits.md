# Credits note: pilot prospecting run, Oct 30, 2026

Workspace: Cargo **GTM Event Oct30**. FullEnrich via its MCP server. Pilot only: about 10 candidates per segment, no scale-up yet.

## Totals

| | Used | Cap | Left under cap | How it was measured |
|---|---:|---:|---:|---|
| Cargo | **31.6** | 1,000 | 968.4 | Sum of `creditsUsedCount` over all 16 Cargo runs (the billing dashboard showed 30.12 at write time, still catching up) |
| FullEnrich | **34** | 1,000 | 966 | Balance 3,000 before, 2,966 after (`get_credits`) |

Nothing else was spent. No emails were sent or scheduled, and no campaign or sequencer was created.

## Funnel

| Segment | Candidates found (Cargo) | Emails found (FullEnrich) | Verified work emails kept |
|---|---:|---:|---:|
| Robotics & Simulation | 10 | 10 | **7** |
| Games | 9 | 9 | **1** |
| 3D Printing | 9 | 9 | **6** |
| Film & VFX | 10 | 6 | **3** |
| **Total** | **38** | **34** | **17** |

Why 21 candidates were dropped:
- 12 had an address FullEnrich did not mark DELIVERABLE (9 "high probability", 3 "catch-all"). Only DELIVERABLE counts as verified.
- 4 had a deliverable address at a different organization (a university, a side company), not the company we targeted.
- 4 had no email found.
- 1 was Canadian, and the address came from enrichment, not a public work page, so CASL rules it out.

Exclusion checks: no competitor, "not ours" company or hobbyist is on the list. No personal webmail. USA only in the final list (the one Canadian was held back for CASL). The Cargo workspace Contacts and Accounts models held 0 records, and the repo has no list of people the founder already knows, so nobody was removed as already known. Check the 17 names against your own contacts before sending.

**Not yet done:** the 17 contacts have not been checked against the founder's own contacts. That check must happen before anything is sent.

## Where the Cargo credits went

| Step | Credits |
|---|---:|
| Sales Navigator probe (1 account) | 0.2 |
| Sales Navigator account search, 85 accounts (Robotics 15, Games 15, Film 15, 3D Printing 40) | 17.0 |
| Sales Navigator lead search, 64 leads (16 per segment) | 12.8 |
| FullEnrich company and people search inside Cargo (3D Printing, used instead of the noisy Sales Navigator results) | 0.0 |
| Sequences: 4 `anthropic.instruct` calls, Sonnet | 1.6 |
| **Total** | **31.6** |

About 11 of those credits went on 3D Printing Sales Navigator searches that came back off-ICP and were discarded.

## Cost per verified contact (pilot actuals, per segment)

Cargo here is each segment's own sourcing spend (searches only). The 1.6 credits of sequence writing is a one-off and does not repeat when scaling.

| Segment | Cargo sourcing | FullEnrich | Kept | Cargo per kept | FullEnrich per kept |
|---|---:|---:|---:|---:|---:|
| Robotics & Simulation | 6.4 | 10 | 7 | 0.91 | 1.43 |
| Games | 6.2 | 9 | 1 | **6.20** | **9.00** |
| 3D Printing | 11.2 | 9 | 6 | 1.87 | 1.50 |
| Film & VFX | 6.2 | 6 | 3 | 2.07 | 2.00 |
| **All (blended)** | 30.0 + 1.6 sequences | 34 | 17 | 1.86 | 2.00 |

FullEnrich bills 1 credit per email found, including the ones we then reject. The 3D Printing Cargo figure includes 11.2 credits of Sales Navigator searches that came back off-ICP and were discarded.

## Projected cost to scale (on top of this pilot)

Each segment is projected at its own pilot rate, for the contacts it still needs (target minus what the pilot kept), then summed. The sequences are already written, so they cost nothing more. Cumulative = pilot spend (Cargo 31.6, FullEnrich 34) plus the new spend.

### 50 per segment

| Segment | Have | Need | Cargo (est.) | FullEnrich (est.) |
|---|---:|---:|---:|---:|
| Robotics & Simulation | 7 | 43 | 39.3 | 61.4 |
| Games | 1 | 49 | 303.8 | 441.0 |
| 3D Printing | 6 | 44 | 82.1 | 66.0 |
| Film & VFX | 3 | 47 | 97.1 | 94.0 |
| **New spend** | 17 | 183 | **522.4** | **662.4** |
| **Cumulative vs 1,000 cap** | | | **554.0: fits** | **696.4: fits** |

### 100 per segment

| Segment | Have | Need | Cargo (est.) | FullEnrich (est.) |
|---|---:|---:|---:|---:|
| Robotics & Simulation | 7 | 93 | 85.0 | 132.9 |
| Games | 1 | 99 | 613.8 | 891.0 |
| 3D Printing | 6 | 94 | 175.5 | 141.0 |
| Film & VFX | 3 | 97 | 200.5 | 194.0 |
| **New spend** | 17 | 383 | **1,074.8** | **1,358.9** |
| **Cumulative vs 1,000 cap** | | | **1,106.4: does NOT fit** | **1,392.9: does NOT fit** |

**Plainly:** 50 per segment fits inside both 1,000-credit caps (Cargo ~554, FullEnrich ~696). 100 per segment does not fit either cap (Cargo ~1,106, FullEnrich ~1,393). Games drives it: at its pilot yield it alone would need ~614 Cargo and ~891 FullEnrich credits for 100.

What would change that: fix the Games yield first. Source studios company-first with Cargo's free FullEnrich search, pass the studio domain into enrichment, then re-pilot 10 Games contacts and re-run this projection. Cargo's FullEnrich `searchCompanies` / `searchPeople` cost 0 credits and gave cleaner 3D Printing results than Sales Navigator; using them for every segment would cut Cargo sourcing close to 0, leaving FullEnrich as the cap that matters.
