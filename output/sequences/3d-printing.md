# 3D Printing: 3-email sequence

- Status: **DRAFT. Not sent, not scheduled, not loaded into any sequencer.** For review first.
- Written by Cargo (`anthropic.instruct`, claude-sonnet-4-6), run `5d606976-fe2e-4328-b6c4-967e41a96473`, from the README pitch, this segment's pains and the README copy rules.
- Sending inbox when approved: caspian@interlinkedfiles.com (the only allowed sender).
- Merge fields: `{{first_name}}`, `{{company}}`. Footer placeholders: `{{sender_name}}`, `{{company_address}}`, `{{unsubscribe_link}}` (fill before any send).
- Recipients: the rows with segment "3D Printing" in `../contacts.csv`.
- Copy-rule check: no em or en dashes, none of the banned words, no competitor names, footer on all 3 emails.

---

## Email 1 (day 0)
**Subject:** when the slicer overwrites your 3MF

Hi {{first_name}},

A slicer update rewrites your 3MF and the settings that printed cleanly last month are gone. No warning, no way back.

Interlinked keeps every save of every STEP and 3MF, so you can step back to the exact file that printed the part you sold.

One price, any team size, works from the desktop app or CLI.

Worth a 15-minute look?

{{sender_name}}
Interlinked | interlinkedfiles.com
{{company_address}}
Not the right person, or rather not hear from us? Reply "unsubscribe" or click {{unsubscribe_link}} and we will not email you again.

## Email 2 (day 3)
**Subject:** reprinting an old order at {{company}}

Hi {{first_name}},

A customer reorders a part from eight months ago. Do you know which STEP and which 3MF printed it?

With Interlinked, you open the desktop app, find that job by date, and reprint from the exact revision. Every save is kept, any file type, any size.

No scramble through USB sticks or old exports.

Happy to show you how it works if that is useful.

{{sender_name}}
Interlinked | interlinkedfiles.com
{{company_address}}
Not the right person, or rather not hear from us? Reply "unsubscribe" or click {{unsubscribe_link}} and we will not email you again.

## Email 3 (day 8)
**Subject:** last note from Interlinked

Hi {{first_name}},

I will keep this short. If protecting every STEP, 3MF and STL so you can reprint exactly what you sold is not a priority right now, no problem at all.

If it is, interlinkedfiles.com is where to start.

{{sender_name}}
Interlinked | interlinkedfiles.com
{{company_address}}
Not the right person, or rather not hear from us? Reply "unsubscribe" or click {{unsubscribe_link}} and we will not email you again.
