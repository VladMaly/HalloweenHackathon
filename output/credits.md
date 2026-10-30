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

## Cost per verified contact (pilot actuals)

- Cargo: 31.6 / 17 = **1.86 credits**
- FullEnrich: 34 / 17 = **2.0 credits** (it bills 1 per email found, including the ones we then reject)
- Per segment, FullEnrich per kept contact: Robotics 1.4, 3D Printing 1.5, Film & VFX 2.0, **Games 9.0** (1 kept from 9 found)

## Projected cost to scale (on top of this pilot)

Uses the pilot rates above. The sequences are already written, so they cost nothing more.

| Target | New verified contacts | Cargo (est.) | FullEnrich (est.) | Running total vs caps |
|---|---:|---:|---:|---|
| 50 per segment | 183 | ~340 | ~370 | Cargo ~372 / 1,000, FullEnrich ~404 / 1,000. Fits. |
| 100 per segment | 383 | ~710 | ~770 | Cargo ~742 / 1,000, FullEnrich ~804 / 1,000. Fits only on the blended rate. |

Risk: at its pilot yield, Games alone would cost about 9 FullEnrich credits per kept contact, so 100 Games contacts could take ~900 credits and break the FullEnrich cap. Before scaling Games: source studios company-first with Cargo's free FullEnrich search and pass the studio domain into enrichment, then re-pilot 10.

Cheaper path: Cargo's FullEnrich `searchCompanies` / `searchPeople` cost 0 credits and gave cleaner 3D Printing results than Sales Navigator. Using them for every segment would cut Cargo spend to roughly the sequence calls, so the cap that matters becomes FullEnrich.
