# Ryker's inbox-support business

> **Moved (Nov 10, 2026):** Outreach now runs in the Guest Support Town (https://claude.ai/artifact/D7Ennyi7ugJcoiGpHM5vzH): prospects, drafts, approvals and sending all live there. `outreach/tracker.csv` is a frozen snapshot from Nov 9 and is no longer updated. Don't add new work to this repo.

One-person service business: answering guest and customer messages (email, web chat,
Facebook/Instagram DMs, vacation-rental platform messages) for small tourism and lodging
businesses between Idaho Falls and Jackson. Started November 2026. Goal: 2 paying clients by Dec 31, 2026.

Source of truth for everything below: the **Business Playbook** doc
https://claude.ai/artifact/8ACvXZtVeFXNKwTSQUQ4ZJ. If something here disagrees with the playbook, the playbook wins.

## Key facts

- Owner: Ryker Kirkham, sole proprietor, Idaho Falls area. Background in sales and customer support.
- Availability: day job about 6 AM to 5 or 6 PM Mountain. Business work happens on weekday evenings (7 to 9 PM) and weekends.
- Service area (remote work): Idaho Falls, Swan Valley, Teton Valley (Driggs, Victor), Island Park, West Yellowstone MT, the Jackson area.
- Offers: a 2-week pilot at $150. Standard at $500/mo. Plus at $800/mo. Holiday ad packs ($300/$500) are add-ons only.
- Promise same-evening replies. Never promise 2-hour replies.
- Season: winter peak runs Dec to Mar. Summer-trip inquiries come in Jan to Apr.

## Agents in this repo

| Agent | File | What it does |
|---|---|---|
| Host outreach | `.claude/agents/host-outreach.md` | Finds lodging/outfitter owners, gets their contact channel, drafts personal first messages and follow-ups, holds every draft for Ryker's approval |

Slash commands: `/outreach [count]`, `/review-drafts`, `/followups`. Details are in `outreach/README.md`.

## Approval rules (from the playbook, non-negotiable)

- **Allowed without asking:** research prospects, find owner names and contact channels, draft messages, update `outreach/tracker.csv`, prepare summaries.
- **Needs Ryker's explicit approval first:** sending any message to a prospect, spending money, agreeing to terms or prices, posting publicly.
- **Never:** ask for or store passwords. Never send fake inquiries to "test" a business. Never invent facts about a business. Never send bulk cold texts. Never promise sales results. Never mention or use the owner's day trading. Never contact the day job's customers.
- Cold emails need a real name and postal address, an honest subject line, and an easy opt-out.
