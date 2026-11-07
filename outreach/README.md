# Host outreach agent

Finds lodging, outfitter and rental-shop owners in the Idaho Falls to Jackson area, drafts a personal
first message for each one, and **waits for your approval** before anything goes out.

## How to use it (from the Claude app, in a session on this repo)

| Say | What happens |
|---|---|
| `/outreach` | Researches the next 15 `new` prospects (Tier 1 first) and walks you through each draft: Approve / Edit / Skip / Do not contact |
| `/outreach 5 Island Park cabins` | A smaller batch focused on one area or type of business |
| `/review-drafts` | Goes back through drafts you haven't decided on yet |
| `/followups` | Drafts the 3-day follow-ups that are due. Add replies like `/followups P004 replied, call Tue` |

A good evening routine is to run `/outreach`, approve the drafts, paste each message into Facebook, Instagram or email,
then tap "sent". Run `/followups` every few days.

## The approval flow

```
new ─▶ researched + drafted ─▶ (you) approve ─▶ (you) send ─▶ sent ─▶ 3 days ─▶ follow-up drafted ─▶ (you) approve ─▶ followed_up
                         └▶ skip / do_not_contact                                   └▶ replied / call_booked / pilot / client / no_reply
```

The agent itself has **no ability to send**. It only has web-research and file tools. Messages go out only when you
send them, or, if you turn on `send_mode: email_via_connector` and connect Gmail, when you approve each email one at a time.

## Files

- `tracker.csv`: one row per prospect. It opens in Google Sheets or Excel.
- `config.md`: your signature, mailing address (legally required for cold email), daily target, and send mode. **Fill in the TODOs before your first emails.**
- `drafts/`: messages waiting for approval.
- `sent/`: messages that went out, kept as a record.
- `../.claude/agents/host-outreach.md`: the agent's instructions, rules and scripts.

## Why it never uses Airbnb messaging

Airbnb and VRBO prohibit using their messaging for solicitation, and doing it can get your account banned.
The agent contacts hosts through their own website, email or Facebook/Instagram page instead.
