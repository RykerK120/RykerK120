---
description: Research prospects and draft first messages for Ryker's approval (default count is daily_target)
argument-hint: "[count] [optional area or category, e.g. 5 Island Park cabins]"
---

Run the outreach batch: $ARGUMENTS

1. Use the `host-outreach` subagent to research and draft first messages for the requested number of
   prospects (default: `daily_target` in `outreach/config.md`). Pass along any area or category the user named.
2. When it returns, show Ryker each draft **one at a time**, laid out for a phone screen:
   - business, channel, send-to address or link
   - the hook and its source link, with a confidence level
   - the full message, ready to copy
   Then ask with AskUserQuestion: **Approve**, **Edit** (Ryker says what to change), **Skip for now**, or **Do not contact**.
3. Apply each answer to `outreach/tracker.csv`:
   - Approve: set `status=approved`. Then act according to `send_mode` in config:
     - `draft_only`: give Ryker the exact text and the link to paste it into, and ask Ryker to confirm once it's sent.
       On confirmation, set `status=sent`, `date_sent` = today, and `followup_date` = today + `followup_after_days`.
       Then move the draft into `outreach/sent/`.
     - `email_via_connector`: this applies only when the channel is Email and a Gmail connector is connected.
       Show the final email (to, subject, body) and send it only after this specific approval. Then log it as above.
       DMs and forms are always sent by Ryker by hand.
   - Edit: revise the draft, show it again, and ask again.
   - Skip for now: set `status=skipped_today`. It returns to `new` on the next run.
   - Do not contact: set `status=do_not_contact`.
4. Never send or mark anything as sent without Ryker's explicit yes for that specific message.
5. Finish with a one-line tally: drafted, approved, sent, skipped. Then commit the tracker and draft changes and push.
