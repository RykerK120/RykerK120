---
description: Walk through drafts already waiting for approval (status drafted or followup_drafted)
---

Read `outreach/tracker.csv` and list every row with `status=drafted` or `status=followup_drafted`.
For each one, open its draft in `outreach/drafts/` and run the same approve/edit/skip/do-not-contact loop
as `/outreach` step 2 onward. Re-check the hook's source link before showing it, because drafts can go stale.

For an approved follow-up, set `followup_sent` = today once Ryker confirms it was sent, and set `status=followed_up`.

When you're done, commit and push the changes.
