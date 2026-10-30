# Games: 3-email sequence

- Status: **DRAFT. Not sent, not scheduled, not loaded into any sequencer.** For review first.
- Written by Cargo (`anthropic.instruct`, claude-sonnet-4-6), run `48aebf12-8fd6-4a25-b0af-8afedab6377f`, from the README pitch, this segment's pains and the README copy rules.
- Sending inbox when approved: caspian@interlinkedfiles.com (the only allowed sender).
- Merge fields: `{{first_name}}`, `{{company}}`. Footer placeholders: `{{sender_name}}`, `{{company_address}}`, `{{unsubscribe_link}}` (fill before any send).
- Recipients: the rows with segment "Games" in `../contacts.csv`.
- Copy-rule check: no em or en dashes, none of the banned words, no competitor names, footer on all 3 emails.
- Edited after generation: removed "no extra charge per gigabyte moved" from email 2 (a claim the README does not support).
- Edited after generation: email 1 said git "will not take the level at all", which is false (git stores binary files). Reworded to the real pain: big binaries bloat git and the large file add-ons get slow, costly and painful at scale. Subject line no longer says "no git".
- Every Games prospect gets all 3 emails. Email 2 has three versions: **2A** for Godot and Blender teams, **2B** for Unity teams, **2C** for Unreal teams. Per the README, do not lead on price with Unity teams, so 2B leads on the project and its history instead of price. Pick by the studio's engine signals (Unity → 2B, Unreal → 2C, Godot or Blender → 2A; unknown → 2A). 2A and 2B were written by hand after generation (no extra credits); 2C is the generated email 2.

---

## Email 1 (day 0)
**Subject:** 40 GB project, lost afternoon

Hi {{first_name}},

If the project is 40 GB, getting it to the team means zips, drives and a lost afternoon. Put the big binary files in git and it bloats, and the usual large file add-ons get slow, costly and painful as the project grows.

Interlinked is one folder for any file type, any size: your umaps, uassets, .blend files and builds, every save kept, the whole team in it from the desktop app on Windows, macOS or Linux.

Worth a 15 minute look?

{{sender_name}}
Interlinked | interlinkedfiles.com
{{company_address}}
Not the right person, or rather not hear from us? Reply "unsubscribe" or click {{unsubscribe_link}} and we will not email you again.

## Email 2A (day 3, Godot and Blender teams)
**Subject:** bandwidth bills on big .blend files

Hi {{first_name}},

Large file bandwidth bills keep growing as the project does. .blend files, textures, .glb exports, full builds: the cost scales with every sync.

With Interlinked, {{company}} pays one price for any team size. Point the desktop app at your project folder, every .tscn scene and .blend file included, and the whole team works from it on Windows, macOS or Linux. Every save of every file is kept.

Does that change anything for you?

{{sender_name}}
Interlinked | interlinkedfiles.com
{{company_address}}
Not the right person, or rather not hear from us? Reply "unsubscribe" or click {{unsubscribe_link}} and we will not email you again.

## Email 2B (day 3, Unity teams)
**Subject:** every save of the scene, kept

Hi {{first_name}},

Scenes, prefabs, FBX and textures grow fast, and getting the whole project to a new teammate still means zips, drives and a lost afternoon.

With Interlinked, {{company}} keeps the project in one folder, any file type, any size, and every save of every asset is kept. Step back to the scene as it was last week, from the desktop app on Windows, macOS or Linux, or from the CLI.

Worth a 15 minute look?

{{sender_name}}
Interlinked | interlinkedfiles.com
{{company_address}}
Not the right person, or rather not hear from us? Reply "unsubscribe" or click {{unsubscribe_link}} and we will not email you again.

## Email 2C (day 3, Unreal teams)
**Subject:** bandwidth bills on big builds

Hi {{first_name}},

Large file bandwidth bills keep growing as the project does. FBX, textures, full builds: the cost scales with every sync.

With Interlinked, {{company}} pays one price for any team size. Drop the Unreal plugin in, point it at your project folder and the whole team works from the desktop app. Every save of every uasset is kept.

Does that change anything for you?

{{sender_name}}
Interlinked | interlinkedfiles.com
{{company_address}}
Not the right person, or rather not hear from us? Reply "unsubscribe" or click {{unsubscribe_link}} and we will not email you again.

## Email 3 (day 8)
**Subject:** closing the loop, {{first_name}}

Hi {{first_name}},

No reply, so I will leave it here. If the timing is off, no problem at all.

One thing worth keeping: Interlinked is built on the same open source engine Epic uses in Unreal Editor for Fortnite. When the project outgrows zips and drives, it is there.

{{sender_name}}
Interlinked | interlinkedfiles.com
{{company_address}}
Not the right person, or rather not hear from us? Reply "unsubscribe" or click {{unsubscribe_link}} and we will not email you again.
