# Iteration 1: pilot prospecting run (Oct 30, 2026)

The first real run of the pipeline in [README.md](README.md). A pilot only: about 10 candidates per segment, nothing sent, nothing pushed.

## Result

- **17 verified work emails** across the four segments, all in the USA: [output/contacts.csv](output/contacts.csv)
- **One 3 email sequence per segment**, drafts only: [output/sequences/](output/sequences/)
- **Spend:** Cargo 31.6 of 1,000 credits, FullEnrich 34 of 1,000 (balance 3,000 before, 2,966 after). Full breakdown: [output/credits.md](output/credits.md)
- **Cost per verified contact:** about 2 Cargo and 2 FullEnrich credits blended. Games was the outlier at 9 FullEnrich credits per kept contact.

| Segment | Candidates (Cargo) | Emails found (FullEnrich) | Verified kept |
|---|---:|---:|---:|
| Robotics & Simulation | 10 | 10 | 7 |
| Games | 9 | 9 | 1 |
| 3D Printing | 9 | 9 | 6 |
| Film & VFX | 10 | 6 | 3 |
| **Total** | **38** | **34** | **17** |

## How people were targeted

1. **Companies:** Cargo's Sales Navigator account search, one search per README segment. For 3D Printing the Sales Navigator results came back off ICP, so that segment used Cargo's FullEnrich company and people search instead (0 credits, cleaner results).
2. **People:** Sales Navigator lead search with the README titles for each segment.
3. **Emails:** FullEnrich enrichment. Only addresses marked **DELIVERABLE** were kept.
4. **Filters applied:** USA and Canada only, at most 2 people per company, work emails only, no competitors, no "not ours" companies, no hobbyists. Each contact row records its consent basis (legitimate interest).

Why 21 of 38 candidates were dropped:
- 12 not marked DELIVERABLE (9 "high probability", 3 "catch-all")
- 4 deliverable, but at a different organization than the one targeted
- 4 no email found
- 1 Canadian whose address came from enrichment, not a public work page (CASL)

## How the emails were written

- Cargo (`anthropic.instruct`) wrote 3 short emails per segment from the README pitch, that segment's pains and the README copy rules.
- Each email opens on one concrete pain for that field (3D Printing: a slicer update overwriting a 3MF that printed fine; Robotics: sensor logs on USB sticks with no lineage; Film: 40 GB of EXRs on drives and transfer links; Games: a 40 GB project moved by zips and drives).
- Then the pitch: every save of any file type and size kept in one place, no USB sticks.
- Close: a soft "Worth a 15 minute look?" and a footer with sender, company address and unsubscribe link.
- Games was edited by hand afterwards: a false claim about git was removed, and email 2 has three versions by engine (Godot or Blender, Unity, Unreal). Unity teams get no price lead, per the README.

**Structure.** Three emails, sent on day 0, day 3 and day 8. Each body is three or four short paragraphs.
- **Email 1 (day 0):** the pain, then the pitch, then "Worth a 15 minute look?" Subjects are short, lowercase and name the pain ("when the slicer overwrites your 3MF", "when the shot moves on a drive").
- **Email 2 (day 3):** a second, sharper angle: 3D Printing reprinting an 8 month old order, Robotics the retirement of NVIDIA Nucleus for Isaac Sim teams, Film AI generations scattered across tools, Games large file bandwidth bills (or, for Unity, every save of the scene kept). It closes with a soft question ("Open to a quick look?", "Does that change anything for you?").
- **Email 3 (day 8):** a short goodbye ("last note from Interlinked", "closing the loop, {{first_name}}"). No meeting ask; it says no problem if the timing is off and restates the pitch in one line.

**Tone.** As the README copy rules ask: plain words in the prospect's own terms (renders, the shot, project files, STEP and 3MF), no em or en dashes, fewer words, no hype. The emails never use the banned words (hosting, server, version control, repository, commit, push, branch, file locking), never name a competitor, never say there is AI inside the product and never lead with the browser link. Each sequence file records this check in its header.

**Personalisation.** Merge fields are `{{first_name}}` (greeting, and the Games and Robotics email 3 subject) and `{{company}}` (email 2). Title is not a merge field. Per segment, the pain, the file types named and the email 2 angle change. Per engine, Games email 2 has three versions: 2A Godot and Blender, 2B Unity, 2C Unreal (unknown engine gets 2A).

**Compliance (CAN-SPAM and CASL).**
- Every email ends with the same footer: sender name, "Interlinked | interlinkedfiles.com", the company's physical address and an unsubscribe line (reply "unsubscribe" or click the link, and we will not email you again).
- Every contact row in [output/contacts.csv](output/contacts.csv) records its consent basis: legitimate interest, cold B2B email to a work address relevant to the person's role, with an opt out in every email.
- CASL: a Canadian address is used only if the work email is publicly published. The one Canadian candidate's address came from enrichment, so they were dropped.
- Still to fill before any send: `{{sender_name}}`, `{{company_address}}` and `{{unsubscribe_link}}` in all four sequences.

## Lessons for iteration 2

- **Games yield is the problem:** 1 kept out of 9. At that rate 100 Games contacts would cost about 614 Cargo and 891 FullEnrich credits. Re-source studios company first with Cargo's free FullEnrich search, pass the studio domain into enrichment, and re-pilot 10.
- **Use Cargo's FullEnrich search for every segment.** It cost 0 credits and beat Sales Navigator on 3D Printing; about 11 Cargo credits went on discarded Sales Navigator results there.
- **Scale estimate:** 50 per segment fits both 1,000 credit caps (Cargo about 554, FullEnrich about 696 cumulative). 100 per segment fits neither.

## Before anything is sent

- Check the 17 names against the people you already know. No such list exists in the repo yet, so this check was not done.
- Fill in `{{sender_name}}`, `{{company_address}}` and `{{unsubscribe_link}}` in every sequence.
- Send only from caspian@interlinkedfiles.com, and warm up the mailbox first.
