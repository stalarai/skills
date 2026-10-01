# Stalar Agent Skills

Break the ceiling on human-led revenue. [Stalar](https://stalar.ai) is the agentic workspace for sales and revenue teams: one sales brain for your data, context and activity, where AI-first sales teams supercharge their work. These Agent Skills bring Stalar into Claude Code, Codex, Cursor and other agents. Your agent handles sales prospecting, lead generation, account research, finding contacts, drafting cold email and LinkedIn outreach, meeting prep and follow-ups through the Stalar MCP server, on your own mailbox, LinkedIn, calendar and CRM. You approve what goes out.

> Stalar is invite only. Ask a teammate or a customer for an invite, or request one at [stalar.ai](https://stalar.ai).

## Install

```bash
npx skills add stalarai/skills
```

Claude Code plugin:

```
/plugin marketplace add stalarai/skills
/plugin install stalar@stalar
```

Then ask your agent to "set up Stalar". The `stalar-setup` skill connects the Stalar MCP server (`https://app.stalar.ai/mcp`) and signs you in.

## What's included

### Setup

| Skill | What it does |
| --- | --- |
| `stalar-setup` | Connects the Stalar MCP server, signs you in, picks the workspace, and walks the Get started checklist: mailbox, LinkedIn, CRM, meeting bot, credits. |

### Prospecting and lead generation

| Skill | What it does |
| --- | --- |
| `prospecting` | Finds new target companies from a plain description of your ICP, or lookalikes of your best customers. |
| `lead-lists` | Grows, refreshes and tidies an existing lead list. |
| `find-contacts` | Finds decision makers at target companies with work emails, phone numbers and LinkedIn profiles. |
| `account-research` | Builds a short, sourced brief on one company before you reach out. |

### Outbound

| Skill | What it does |
| --- | --- |
| `outreach-sequence` | Writes cold email and LinkedIn sequences, personalized per prospect, and previews them on real leads. |
| `cold-outreach` | Launches a campaign to a lead list from your own mailbox or LinkedIn, and pauses or changes it. |
| `outreach-results` | Reports replies, meetings booked and campaign stats, and clears messages waiting for approval. |

### Daily selling

| Skill | What it does |
| --- | --- |
| `sales-briefing` | Your day in one list: meetings to prepare, replies to answer, follow-ups owed, approvals. |
| `meeting-prep` | Briefs you before a sales call: attendees, account history, open threads, questions to ask. |
| `meeting-follow-up` | Turns a recorded meeting into a recap and a follow-up email ready to send. |
| `email-replies` | Reads prospect replies and drafts answers in your voice. |

## How it works

Each skill is a short routine your agent follows. It calls tools on the Stalar MCP server, which does the work: company and people search, contact enrichment, sequence writing, sending from your own accounts, meeting notes and your CRM. After you sign in, the skills load Stalar's detailed guides and your team's own skills (tone of voice, ICP) from the server, so they stay current without reinstalling.

Nothing that sends or spends credits runs without a preview and your yes.

## FAQ

**How do I get access?** Stalar is invite only. Ask a teammate or a customer for an invite, or request one at [stalar.ai](https://stalar.ai). Once you have an account, `stalar-setup` connects your agent.

**Which agents does it work with?** Any agent that supports Agent Skills and MCP servers, including Claude Code, Codex and Cursor.

**Does it send emails on its own?** No. Every send, campaign launch and paid search shows a preview first and waits for your approval.

**Where do the leads and contact details come from?** From Stalar's company and people search and enrichment, plus what is already in your inbox, calendar and CRM.

**Does it work with my CRM?** Stalar connects to HubSpot, Salesforce, Attio and Upsales.

**Does installing the skills cost anything?** No. Workspaces in Stalar's Get started program earn credits for connecting them.

## Links

- [Stalar](https://stalar.ai)
- [Sign in](https://app.stalar.ai)

## License

MIT
