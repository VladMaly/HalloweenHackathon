# HalloweenHackathon

GTM Fellowship Halloween Hackathon, Oct 30, 2026 (Digital Jungle SF).

Our entry: a GTM prospecting machine for **Interlinked**, built with Cargo, FullEnrich and Nenya.

**Latest run:** [Iteration 1](ITERATION-1.md): 17 verified work emails, 4 draft sequences, 31.6 Cargo and 34 FullEnrich credits used. Nothing sent.

## What Interlinked is

**FILE COLLABORATION: ANY SIZE, ANY TYPE**
**Build anything together**

Title tag: `Interlinked | File collaboration for any size, any type`

Said out loud: "It's file collaboration, primarily for robotics, games and 3D printing."

Interlinked (interlinkedfiles.com) shares and hosts projects: one folder of work in progress, any file type, any size. Every save is kept, and the team works in it from the desktop app (Windows, macOS, Linux), the command line or their AI agents (MCP). No seats: one price for any team size.

If they ask "doesn't Drive or GitHub do that?": "Drive can't handle a game project, and GitHub chokes on anything big. We do both in one place."

### The four field cards

No TB numbers; a Higgsfield video on each card.

| # | Card | Higgsfield video |
|---|---|---|
| 1 | **Robotics & Simulation** | A robot arm in a lab |
| 2 | **Games** | A castle and river landscape |
| 3 | **3D Printing** | The F1 steering wheel nozzle shot |
| 4 | **Film & VFX** | An LED wall film set |

## The goal

Build a GTM system that actually runs, such as a list, a sequence or a campaign that went out, and demo it live at 4:00 PM (3 minutes, no slides).

Judges score:
1. It works live.
2. It produced real output.
3. It kept the team's rules (suppression list, consent, credit budget) for the whole run.
4. It uses Nenya, Cargo and FullEnrich.

## Ideal customer profiles (ICPs): who we prospect

Sourced from the Interlinked branding document in CellsInterlinked and its marketing research (not invented here):
- `CellsInterlinked/docs/BRAND.md` (section 2, the four fields, which `docs/INTERLINKED_2026.md` names as the ICPs; section 10, the field cards)
- `CellsInterlinked/docs/atScale/marketing/WHO_NEEDS_IT_TODAY.md` (the ranking of who needs it today and can switch)
- `CellsInterlinked/docs/atScale/marketing/RESEARCH_2026-10-23.md` (the ICPs that need it today: AI video studios first, boutique VFX and post second, games first on the homepage)

Every ICP those files name, and where it sits here:

| ICP in the sources | Source | Here |
|---|---|---|
| Robotics & Simulation (the lead field) | BRAND.md s2, s10 | 1, primary |
| Games (indie: Unreal, Godot, Blender) | BRAND.md s2, s10; WHO_NEEDS_IT_TODAY #3; RESEARCH | 2, primary |
| Hardware teams and print farms (3D Printing) | BRAND.md s10 (proposed 2026-10-30, not settled); WHO_NEEDS_IT_TODAY #4 | 3, primary |
| Boutique VFX and post, freelancers (Film & VFX) | BRAND.md s2, s10; WHO_NEEDS_IT_TODAY #2; RESEARCH (second) | 4a, secondary |
| AI video studios doing client work (Film & VFX) | WHO_NEEDS_IT_TODAY #1; RESEARCH (lead ICP this month) | 4b, secondary field, highest urgency |
| Solo builders across machines | WHO_NEEDS_IT_TODAY #5 | Not prospected: a free on-ramp, not a payer |
| BIM (Revit) | WHO_NEEDS_IT_TODAY #6; RESEARCH | Skip (except SketchUp and Rhino studios) |
| Medical imaging | BRAND.md s2 (card 4: "the most money, but gated", later); WHO_NEEDS_IT_TODAY #7; RESEARCH | Skip: locked in (PACS, HIPAA); s10 proposes taking it off the cards |

Common to all (BRAND.md s2): "teams whose work in progress is big files, in fields that grow fast with AI", doing complex, layered work; small to mid-sized (the sources say "small teams", "small shops", "indie", "a 30 person team"), who hate per-seat storage. **Not ours** (BRAND.md s2): AI models (Hugging Face holds them), the legacy engineering firms, the big VFX houses that own their own storage (won later, by a VFX page and an email). **Skip for now** (WHO_NEEDS_IT_TODAY, RESEARCH): medical imaging and BIM, both locked in.

How to read the filters: **industries and pains are from the source**. Headcount ranges and titles are our working translation of the source's "small teams" and roles into Cargo and FullEnrich filters; adjust them live if the list comes back thin. Geos are not stated in the source; for this run, USA and Canada (we sell worldwide, so expand later).

**Priority:** Robotics & Simulation, Games and 3D Printing are the **primary** segments (the three said out loud). Film & VFX is **secondary**: it is on the page but not in the spoken line.

### 1. Robotics & Simulation (primary, the lead)

- **Who:** robotics startups and teams running simulation, especially small Isaac Sim teams; very well funded right now, the biggest payer with the weakest tools.
- **Industries:** Robotics, Automation / Industrial Automation, Autonomous Vehicles and Drones, Computer Software (simulation).
- **Headcount:** 10 to 200.
- **Titles:** CTO, VP / Head of Engineering, Head of Robotics, Robotics Software Lead, Simulation Lead / Simulation Engineer, ML / Data Infrastructure Lead, Founder (under 30 people).
- **Pains (their words):** "Sensor logs scattered across S3 buckets, and nobody knows which dataset trained which model." Logs moved off robots on USB sticks, no way to version bags against newer software. NVIDIA deprecated Omniverse Launcher, Nucleus Workstation and Nucleus Cache (Oct 1, 2025), so small Isaac Sim teams lost their free collaboration layer for sim assets.
- **Today they use:** rosbag2 / MCAP plus scripts, Foxglove (viewing, not versioning), Hugging Face (LeRobot), DVC or raw S3.
- **Their files:** sensor logs (MCAP, rosbag: camera, lidar, IMU), tens of GB per robot per hour; sim scenes and robots (USD, URDF, MJCF); meshes and CAD (STL, OBJ, glTF, STEP); datasets and models (Parquet, MP4, safetensors, PT checkpoints).
- **Why Interlinked:** "one place for sim assets, datasets and logs, versioned together" (BRAND.md's pitch; in outreach say "every save kept", not "versioned"). Linux desktop app and CLI ship today (Ubuntu / ROS teams covered).
- **Signals / keywords:** ROS / ROS 2, Isaac Sim, Omniverse, Nucleus, MCAP, rosbag, URDF, MJCF, USD, LeRobot, Foxglove, DVC, "simulation", "sensor data", "fleet"; job posts for robotics or simulation engineers; recent funding.

### 2. Games (primary)

- **Who:** indie and small game studios on Unreal, Godot and Blender (the research's list); Unity teams too, but not on price. Smaller data, indie budgets, the most crowded field.
- **Industries:** Computer Games, Video Games / Interactive Entertainment.
- **Headcount:** 2 to 50.
- **Titles:** Founder / Studio Head, Technical Director, Lead Developer / Lead Programmer, Art Director / Lead Artist, Producer.
- **Their files:** engine files (uasset, umap, Unity scenes and prefabs); source art (FBX, blend, Substance, PSD); textures and audio (EXR, PNG, TGA, WAV). Projects run 50 GB to several TB.
- **Pains:** "The project is 40 GB. Getting it to the team means zips, drives and a lost afternoon." Git does store the level, but a project of big files bloats it, and the large file add-ons (Git LFS) get slow, costly and painful as the project grows: GitHub counts every clone and CI download against the owner. (BRAND.md's card quote also says "git will not take the level at all"; that half is false, so we don't use it.)
- **Today they use:** Perforce, Git LFS on GitHub, Diversion, Anchorpoint, Unity Version Control, other Lore hosts (crowded field).
- **Why Interlinked:** "Your level and .blend history without LFS bandwidth bills." Built on Lore, Epic's open source version control, built into Unreal Editor for Fortnite (say "Unreal Editor for Fortnite", never "from Fortnite"). An Unreal plugin is the games funnel (code written, launch planned).
- **Signals / keywords:** Unreal Engine, Godot, Blender, Unity (do not lead on price with Unity teams: Unity Version Control has no seat charges since 2026-03-01), "indie studio", Git LFS, Perforce, uasset / umap, FBX, Substance; job posts for Unreal developers or technical artists.

### 3. 3D Printing (primary: hardware teams and print farms)

- **Who:** hardware teams and print farms, not hobbyists (hobby files are small; the payers are teams).
- **Industries:** Mechanical / Industrial Engineering, Consumer Electronics, Additive Manufacturing / 3D Printing, Product Design.
- **Headcount:** 5 to 200.
- **Titles:** Founder, Head of Hardware, Mechanical Engineering Lead, Product Design Lead, Print Farm / Production Manager, Operations Manager.
- **Their files:** STEP and CAD assemblies, 3MF slicer projects (for a whole fleet of printers), STL, scan data. Hobby files are small, so the case is many parts and revisions, not one big file.
- **Pains:** old 3MF files print "a total mess" after a slicer update; Bambu Studio overwrites 3MFs unasked; GrabCAD Workbench shut on 2023-06-01 and deleted its files; Onshape Free no longer makes private documents.
- **Today they use:** slicer project files (Bambu Studio), GrabCAD (gone), Onshape, MakerWorld for sharing.
- **Why Interlinked:** "Reprint exactly what you sold: every STEP and 3MF, every save." Step back to the exact file that printed.
- **Signals / keywords:** "print farm", "additive manufacturing", "rapid prototyping", Bambu Lab, Prusa, 3MF, STEP, STL, slicer, GrabCAD, Onshape, SolidWorks, Fusion 360; companies selling printed parts or products.
- **Caution (from the brand file):** hobby print files are small STLs, so skip hobbyists and makers; target teams with many parts and revisions.

### 4. Film & VFX (secondary field, two ICPs)

People making AI video see themselves in "Film" (BRAND.md), so both ICPs below sit under the Film & VFX card. The 2026-10-23 research ranks them first and second for urgency this month.

#### 4a. Boutique VFX and post, freelancers

- **Who:** small remote VFX and post houses and the freelancers they hire; work is moving to them as big houses close (Technicolor's MPC and The Mill, Glassworks).
- **Industries:** Motion Pictures and Film, Media Production, Animation, Post-production, Broadcast Media.
- **Headcount:** 2 to 100.
- **Titles:** Founder / Executive Producer, Studio Manager, VFX Supervisor, Head of Pipeline / Pipeline TD, Post-production Supervisor, Compositing Lead.
- **Pains (their words):** "The shot is forty gigabytes of EXR, and it moves between artists on drives and transfer links." Versions by hand as `shot_v001`; WeTransfer cut free use; per-seat storage they pay for themselves.
- **Today they use:** LucidLink (streams, not versioned), ShotGrid / ftrack (tracking), Frame.io (review), Perforce at larger studios, Dropbox and a NAS at small shops.
- **Their files:** camera RAW (R3D, BRAW, ARRIRAW), hundreds of GB per shoot day; EXR image sequences, GBs a shot; sim caches (VDB, bgeo, Alembic), often the biggest files in the studio; scenes (Houdini, Nuke, Maya, USD).
- **Why Interlinked:** "one tool that streams and versions, in place of LucidLink plus Perforce" (BRAND.md), sold as the storage and versioning layer beside the tracker, not a replacement for it (WHO_NEEDS_IT_TODAY); every version of the shot, one link for the client, no seats. Gap: no Nuke, Resolve or Premiere plugin yet.
- **Signals / keywords:** "VFX studio", "post-production", "boutique", "compositing", Houdini, Nuke, EXR, ShotGrid / Flow Production Tracking, ftrack, LucidLink, Frame.io; small remote teams that use freelancers.
- **First message (from the research):** "Every version of the shot, one link for the client, no seats."
- **Caution:** studios subcontracting freelancers may require security audits (MPA Trusted Partner Network); not checked.

#### 4b. AI video studios doing client work (the lead ICP in the 2026-10-23 research)

- **Who:** studios and creators producing AI video for clients with Higgsfield, Kling, Runway, Veo and Midjourney; no incumbent, near-zero switching cost.
- **Industries:** Media Production, Advertising Services, Marketing Services, Motion Pictures and Film, Online Media.
- **Headcount:** 1 to 50.
- **Titles:** Founder / Creative Director, AI Video Producer, AI Filmmaker / Generative Artist, Head of Production, Content Lead.
- **Pains:** hundreds of generations per short film, every client revision multiplies it; work lives inside each tool and then in Downloads folders; tools cap or cut storage and archive access. (Do not say "Higgsfield deletes your work": not confirmed.)
- **Today they use:** each tool's own library, Downloads folders, n8n and Zapier pipelines; Higgsfield's team workspace is the threat.
- **Why Interlinked:** one history across every model, with each generation's prompt, plus the edit, plus one link the client opens.
- **Signals / keywords:** "AI video", "AI film", "generative video", "AI studio", "AI commercials", Higgsfield, Kling, Runway, Veo, Midjourney, n8n, Zapier.
- **First message (from the research):** "Every generation from every model, with its prompt, in one link your client opens."

### Exclude from every list

- **Competitors** (named in the sources): Perforce, Diversion, Anchorpoint, Unity, LucidLink, Suite Studios, Frame.io, Autodesk (ShotGrid), ftrack, Foxglove, Dropbox, Onshape / PTC, GrabCAD, Higgsfield (sells a team workspace). Do not email their staff.
- **Not ours:** AI model hosts (Hugging Face), legacy engineering firms, big VFX houses with their own storage.
- **Skip for now:** BIM (Revit) firms (except SketchUp and Rhino studios), medical imaging.
- **Hobbyists, solo makers and solo builders:** a free on-ramp, not payers.

### Copy rules for outreach (from the brand file)

- No em dashes or en dashes. Fewer words. Their words: renders, footage, project files, the level, the shot. Nobody says "binary files".
- Never say in ads, posts or outreach: hosting, server, version control, repository, commit, push, branch. Never say "file locking". Never name a competitor in an ad. No internal codenames.
- Never describe Interlinked as having AI inside it: agents drive it, there is no model in the product.
- Never lead with the browser link or "nothing to install": the desktop app, CLI and MCP are the product.

## Overview: what this project does

1. **Cargo builds the prospect list** from the ICPs above: companies by industry and headcount, then people by title, in the workspace **GTM Event Oct30**.
2. **FullEnrich finds verified work emails** for those people (work emails only, no personal addresses).
3. **Cargo writes personalized outreach** per field, using each segment's pain and "why Interlinked", as a sequence / campaign.
4. **Nenya keeps the team's rules for the whole run:** suppression / do-not-contact list checked before any send, work emails only, credit budget never exceeded. See [NENYA.md](NENYA.md).
5. **Everything lands in `output/`** (the contact list, one sequence per segment, the credits note) and **nothing is sent without review**: the founder checks the list and the copy first.

### Team rules

Decided Oct 30, 2026.

| Rule | Value |
|---|---|
| Cargo credit cap | 1,000 credits |
| FullEnrich credit cap | 1,000 credits |
| Do-not-contact / suppression list | Brand new contacts only (no one we already know), plus competitors and "not ours" (list above), plus anyone who opted out |
| Sending inbox | caspian@interlinkedfiles.com |
| Countries | USA and Canada |
| Consent basis | Legitimate interest: cold B2B email to work addresses, relevant to the person's role, easy opt out. Each contact records its basis. Canadian contacts only if their work email is publicly published (CASL). |
| Work emails only | Yes |

**The pitch:** we replace USB sticks and legacy software with one place that scales to any file type and any size.

## Tools

In one line each:
- **Cargo:** finds the companies and people who fit our ICPs and writes the outreach to them.
- **FullEnrich:** turns those names into verified work emails we can actually reach.
- **Nenya:** watches the agents doing the work so they stick to our rules (do-not-contact list, consent, credit cap) for the whole run.

### Cargo
- What it is: GTM platform for list building, enrichment, workflows and agents.
- Access: `cargo-ai` CLI, plus the Cargo skills in Claude Code. Web app: https://app.getcargo.io
- Workspace for this event: **GTM Event Oct30** (`c6343fbc-ad6f-4a12-9cb7-3c2309fc149b`)
  - Claude Code uses it automatically in this repo (`CARGO_WORKSPACE_UUID` in `.claude/settings.json`).
  - In a plain terminal: `$env:CARGO_WORKSPACE_UUID='c6343fbc-ad6f-4a12-9cb7-3c2309fc149b'`
- Other workspace: **Personal**, the CLI's default login.
- Login check: `cargo-ai whoami`

### FullEnrich
- What it is: B2B contact enrichment (verified emails, phone numbers) and people/company search.
- Access: MCP server `fullenrich` (`https://mcp.fullenrich.com/mcp`) in Claude Code, signed in with OAuth. Web app: https://app.fullenrich.com
- Credits: 3,000 as of Oct 30, 2026.
- Login check: in Claude Code, run `/mcp` and look for `fullenrich`.

### Nenya (Durable Intelligence)
- What it is: keeps AI agents on the rules and commitments the team sets.
- Installed: Nenya 1.0.3 (Oct 30, 2026), via `npx -y @qwntllabs/nenya setup`.
- Details, commands and our team rules: see [NENYA.md](NENYA.md).

### Claude Code
- Drives Cargo (CLI and skills), FullEnrich (MCP) and Nenya from this repo.

## Notes
- Check the credit cost before any enrichment or export.
- FullEnrich export links expire after 24 hours, so save output files into this repo.
- Never commit API tokens or credentials.
