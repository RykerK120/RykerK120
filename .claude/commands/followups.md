---
description: Draft 3-day follow-ups that are due, then review them, and log replies Ryker got
argument-hint: "[optional: replies, e.g. 'P004 replied, wants a call Tue']"
---

$ARGUMENTS

1. If Ryker reported replies, update those rows first. Use `replied`, `call_booked`, `pilot`, `client`,
   `declined` or `do_not_contact`, and add a dated note. A "no thanks" always becomes `do_not_contact`.
2. Use the `host-outreach` subagent to draft follow-ups for rows that are `sent`, where `followup_date` is today
   or earlier and `followup_sent` is empty. It sends only one follow-up per prospect.
3. Review them with Ryker using the `/review-drafts` loop.
4. End with this week's numbers from the tracker: messages sent, replies, reply rate, calls booked, pilots, and clients.
   Then commit and push.
