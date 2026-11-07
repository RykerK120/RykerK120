# Outreach config

The agent reads this file before drafting.

- sender_name: Ryker Kirkham
- business_name: Upper Valley Guest Support
- reply_email: uppervalleyguestsupport@gmail.com
- phone: (none in signature)
- mailing_address: 501 Pleasant County Ln, Rigby, ID 83442
- daily_target: 15
- followup_after_days: 3
- timezone: America/Denver
- send_mode: email_via_connector
  # draft_only: Ryker sends every approved message by hand (copy and paste).
  # email_via_connector: approved *emails* get sent from the main session through a connected Gmail
  #   connector after Ryker approves each one. DMs and forms are always sent by Ryker by hand.

## Email signature (appended to every cold email, exactly as written)

```
Thanks,

Ryker Kirkham
Upper Valley Guest Support
uppervalleyguestsupport@gmail.com
501 Pleasant County Ln, Rigby, ID 83442

Not interested? Reply "no thanks" and I won't contact you again.
```

DMs and website forms end with "Thanks, Ryker (Upper Valley Guest Support)" and need no address or opt-out line.

## Gmail connector notes

- Connected account must be uppervalleyguestsupport@gmail.com. Before the first send in a session, confirm the connector's account matches `reply_email`. If it doesn't, stop and tell Ryker.
- Every email still needs Ryker's per-message approval. The connector only removes the copy-paste step.
- If the connector can only create drafts, put each approved email in Gmail Drafts, tell Ryker it's ready to send, and mark it `sent` only after Ryker confirms.
- If no Gmail connector is available in the session, fall back to draft_only.
