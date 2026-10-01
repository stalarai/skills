# CLAUDE.md

Guide for working on this repo. Read it before adding or changing a skill.

## The split: routine here, detail on the server

These skills are public. Each one holds only what the agent needs to pick it up and start: the trigger words, the inputs, the first one to three Stalar MCP tools, the guardrails and the handoffs. The detailed workflow (how to search, how to write copy, the personalization inputs) lives behind sign-in on the Stalar MCP server and is read with `skills_list` and `skills_load`. Never copy that detail into a SKILL.md.

## Skill shape

Every `skills/<name>/SKILL.md` has, in order: frontmatter (`name`, `description`), a one-line purpose, Required inputs, Start, Workflow (three or four numbered steps), Guardrails, Handoffs.

- **Names** are the words a rep would say (`prospecting`, `email-replies`). Only `stalar-setup` carries the prefix.
- **Descriptions** decide when the agent loads the skill. List the words users say, with synonyms, and point at the sibling skill for nearby requests so two skills never claim the same words.
- **Start** is always: `skills_activate` with the skill's name once per session, then `skills_list` and `skills_load` for the matching guide.
- **Tools**: name only the first one to three tools. Every tool named must exist on the Stalar MCP server.
- **Copy**: plain words, no em dashes.

## Adding a skill

1. The Stalar MCP server must accept its name in `skills_activate` first; a name it does not know is rejected.
2. Add the skill directory, a row in the README table for its group, and a CHANGELOG entry.
3. Check every tool it names against the server's tool list.
