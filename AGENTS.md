# AGENTS.md

Guide for agents and contributors working on this repository.

## What this is

A single portable Agent Skill named `can-do` (the NoBrainer Can-Do Approach): an operating guide that tells an AI agent to finish the requested work, make routine decisions, recover from failures and verify the result. It does not change the host's permissions or the user's approval gates. There is no code, build or test suite; the repository is documentation.

## Layout

| Path | Purpose |
|---|---|
| `SKILL.md` | The skill. YAML frontmatter (`name: can-do`, `description`) followed by 16 numbered sections and a "Final completion check". |
| `README.md` | Public description, usage and install notes. |
| `references/sources.md` | Source provenance, portability choices, coverage table and writing-style measurements. Not needed for routine use. |
| `assets/nobrainer-tech.svg` | Logo used in the README. |

## Working on it

- Keep `references/` beside `SKILL.md`; clients that install the repository as a skill rely on that layout.
- Do not rename the skill (`name: can-do`) or change the frontmatter `description` casually: clients use it to decide when to load the skill.
- Section numbers in `SKILL.md` are referenced by the "Coverage of the portable guide" table in `references/sources.md`. If you add, remove or reorder sections, update that table and the "16 areas" wording in `README.md`.
- The guide is written in short, direct sentences of simplified technical English with concrete terms. Match that style: no filler, no promotional wording, one idea per sentence.
- Keep the guide host-neutral. Do not name specific tools, models, paths or services as requirements; it must work across models and agent environments.
- The guide must stay within the host's instruction hierarchy: it adds a working method and never grants authority, bypasses approvals or changes safety rules.
- Claims in `references/sources.md` are tied to dated, pinned sources. When you update the guide from new sources, record the date checked and the pinned revision; do not claim vendor provenance that was not verified.
- Do not copy third-party prompt text into the repository. The guide uses original wording.

## Checks

No automated checks exist. Before opening a PR, read `SKILL.md` top to bottom, confirm the frontmatter is valid YAML, confirm relative links in `README.md` resolve, and check that the README's description of the files still matches the repository.
