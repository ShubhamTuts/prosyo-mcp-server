---
name: prosyo-outbound
description: >
  Use Prosyo's hosted MCP for LinkedIn and email outbound from Cursor.
  Read tools return data immediately. Writes that send, enroll, launch,
  unlock, research, or spend credits wait for an explicit yes in chat
  before confirm_action.
---

# Prosyo outbound

Prosyo MCP is the hosted server at `https://app.prosyo.com/ai`. There is no API key and no local process. The first connection opens a browser allow screen so the workspace can be chosen.

## Tool use

- Call read tools (overview, campaigns, lists, inbox, intent) when they answer the question.
- For a write that sends a message, launches or resumes a campaign, enrolls people, unlocks intent leads, researches or enriches prospects, or approves a review that spends credits: show what will happen and wait. Call `confirm_action` with the returned `confirmation_token` only after the user confirms in chat.
- `pause_campaign` and `save_intent_leads_to_list` apply immediately.
- `create_campaign` stays a draft. It does not launch or enroll anyone.
