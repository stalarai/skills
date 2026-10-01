---
name: stalar-setup
description: "Set up Stalar for this agent: connect the Stalar MCP server, sign in, pick the workspace, see credits and the Get started checklist, and connect email, LinkedIn, CRM and the meeting bot. Use when Stalar tools are missing, the user is new to Stalar, asks how to get started, hits a paywall or is out of credits, or wants to connect an account or invite teammates."
---

# stalar-setup

Get this agent connected to Stalar and the workspace ready to sell from.

## Required inputs

A Stalar account. Stalar is invite only: if the user has none, say so and point them to https://stalar.ai to request an invite, or to ask a teammate or a customer for one. Then stop.

## Start

1. Once per session, before any other Stalar call: `skills_activate` with `{ "skill": "stalar-setup" }`. If no Stalar tools are available, use stalar-setup first.
2. `skills_list`, then `skills_load` any of the user's or team's own skills that fit (tone of voice, ICP).

## Workflow

1. If no Stalar tools are available, add the MCP server `stalar` at `https://app.stalar.ai/mcp` in this agent and sign in when the browser opens. Then restart the agent session.
2. `onboarding_status_get`: confirm the workspace with the user and read the Get started checklist. Offer the next open step.
3. Connect what the checklist asks for through the links the Stalar tools return (mailbox, LinkedIn, CRM, meeting bot). The user finishes each connection in the browser.
4. `billing_status_get` when a tool returns a paywall: show the link and stop until the user is back.

## Guardrails

- Never ask for passwords or API keys in the chat. Every connection happens in the browser.
- Installing the skills earns credits once per user in workspaces in the Get started program; say so only when `onboarding_status_get` lists the step.

## Handoffs

Prospecting to find target companies, sales-briefing for what to do today.
