# Palimnote Templates

Copy-and-fill templates and checklists for projects, launches, incidents and talks. Plain Markdown: paste one into any AI assistant or fill it in by hand. Most templates live in their own repository; this repo is the index, plus two checklists.

## Works with

| Surface | How | Status |
| --- | --- | --- |
| ChatGPT, Gemini, Claude.ai | Paste the template file into the chat with your notes and ask it to fill the slots | Plain text, no setup |
| Codex, Cursor, Aider, Jules | Copy the file into your project; the repo's `AGENTS.md` describes how to edit this catalog | Plain text, no setup |
| Claude Code, Gemini CLI, Copilot | Same copy step; `CLAUDE.md`, `GEMINI.md` and `.github/copilot-instructions.md` point to `AGENTS.md` | Plain text, no setup |
| By hand | Copy the file, replace the slots, tick the boxes | Works offline |

These are text templates, so no assistant integration is needed or claimed beyond reading Markdown.

## Templates

| Template | Description |
| --- | --- |
| [incident-runbook-template](https://github.com/hyderhusainarastu/incident-runbook-template) | A fill-in incident runbook that forces failure classification before log-reading and requires every ranked failure signature to carry an explicit non-evidence caveat. |
| [launch-campaign-scaffold-kit](https://github.com/hyderhusainarastu/launch-campaign-scaffold-kit) | A directory scaffold and default-deny governance system for a product, crowdfunding or marketing launch: one JSON manifest with a publication kill switch, claims and rights ledgers where nothing publishes until its row reads cleared, and two dependency-free Node tools for validating the manifest and checksumming an assets archive. |
| [project-memory-file-scaffold](https://github.com/hyderhusainarastu/project-memory-file-scaffold) | A blank memory file for a long-running project, loaded at the start of every working session to say where things stand. |
| [cross-session-agent-handoff-prompt-template](https://github.com/hyderhusainarastu/cross-session-agent-handoff-prompt-template) | A fill-in template for the message you write when work moves from one AI-agent session to another. |
| [pnpm-monorepo-ci-template](https://github.com/hyderhusainarastu/pnpm-monorepo-ci-template) | A ready-to-copy `ci.yml` for pnpm workspaces: install, migrate, lint, typecheck, test, build and Playwright E2E. |
| [pre-publication-review-gate-checklist](https://github.com/hyderhusainarastu/pre-publication-review-gate-checklist) | A pre-launch review gate for public-facing content. |

## Checklists in this repo

| Checklist | Description |
| --- | --- |
| [checklists/talk-preflight.md](checklists/talk-preflight.md) | Talk-day preflight with `{date}`, `{room}` and `{timezone}` variables: no-sleep and no-notification settings for macOS, Windows and Linux, extended display, offline and USB backups, back-of-room check, projector-failure plan and a fallback ladder. |
| [checklists/qa-seeds-template.md](checklists/qa-seeds-template.md) | A template for preparing Q&A answers from your own paper: say so when the paper has no answer, and mark outside facts for verification. |

For slides, see [syntax-deck](https://github.com/hyderhusainarastu/syntax-deck) (an offline slide engine, work in progress), which links to the talk preflight checklist.

## Companions

`launch-campaign-scaffold-kit` pairs with [pre-publication-review-gate-checklist](https://github.com/hyderhusainarastu/pre-publication-review-gate-checklist): run the review gate before flipping the launch manifest's kill switch. Before a public push, [release-privacy-scanner](https://github.com/hyderhusainarastu/release-privacy-scanner) can scan a repository, its history and archives for leaks.

## More from the hub

New repositories that pair well with these templates.

| Repository | What it does |
| --- | --- |
| [multi-agent-orchestration-playbook](https://github.com/hyderhusainarastu/multi-agent-orchestration-playbook) | Twelve rules for running teams of AI agents, an `AGENTS.md` template to drop into a project, and tested helper scripts. |
| [ai-coding-agent-guardrail-hooks](https://github.com/hyderhusainarastu/ai-coding-agent-guardrail-hooks) | A tool-neutral `guardrails check` CLI, a Claude Code hook adapter and git hooks that keep `.env` values out of commits. Advisory, not a sandbox. |
| [agent-report-evidence-gate](https://github.com/hyderhusainarastu/agent-report-evidence-gate) | A CLI that checks an AI agent's "done" report for evidence completeness. |
| [release-privacy-scanner](https://github.com/hyderhusainarastu/release-privacy-scanner) | Scans a repository, its git history and release archives for publication leaks. |
| [safe-mcp-server-template](https://github.com/hyderhusainarastu/safe-mcp-server-template) | A Python template for an MCP server that treats tool output as untrusted. |
| [deep-research-skill](https://github.com/hyderhusainarastu/deep-research-skill) | An agent skill for auditable research: a saturation stop rule and explicit verification levels. |
| [cross-model-second-opinion](https://github.com/hyderhusainarastu/cross-model-second-opinion) | An agent skill for getting a budgeted second opinion from a different AI model. |
| [hallucinated-citation-checker](https://github.com/hyderhusainarastu/hallucinated-citation-checker) | Checks every BibTeX entry against Crossref, OpenAlex, arXiv, Open Library and doi.org. |
| [scholarly-citation-resolver](https://github.com/hyderhusainarastu/scholarly-citation-resolver) | Resolves a free-text citation to verified metadata from six open scholarly sources. |
| [local-first-llm-router](https://github.com/hyderhusainarastu/local-first-llm-router) | A policy layer that tries a script, then a local model, and escalates to a cloud model only when checks fail and the data's privacy tier allows it. |
| [ollama-memory-governor](https://github.com/hyderhusainarastu/ollama-memory-governor) | Keeps free RAM above a floor on a machine running several Ollama models. |

## Quick start

- **ChatGPT, Gemini, Claude.ai:** open a template or checklist, paste it into the chat with your notes, and ask the assistant to fill the slots. Check the result yourself.
- **Codex, Cursor, Claude Code, Gemini CLI, Copilot:** copy the file into your project folder, then ask the assistant to fill it from your notes.
- **By hand:** copy the file and replace each slot. Slots are written as `{name}` in the checklists and as placeholders in each template repository; see that repository's README for its own setup.

## Example

Take `checklists/talk-preflight.md`. Its header reads:

```
Variables:
- `{date}` : day and start time of the session
- `{room}` : where you present
- `{timezone}` : the time zone of the room, for example `America/Denver`
```

Fill them in (`{date}` = "2026-03-14 09:30", `{room}` = "Hall B", `{timezone}` = "America/Denver") and the checklist's opening line becomes: "Talk: 2026-03-14 09:30, room Hall B, clock set to America/Denver." Then work through the numbered sections and tick each box.

## Related catalogs

| Catalog | Description |
| --- | --- |
| [palimnote-skills](https://github.com/hyderhusainarastu/palimnote-skills) | Portable agent skills following the SKILL.md convention. |
| [palimnote-tools](https://github.com/hyderhusainarastu/palimnote-tools) | Standalone tools and scripts. |
| [palimnote-agent-patterns](https://github.com/hyderhusainarastu/palimnote-agent-patterns) | Reusable agent persona and orchestration patterns. |

## License

CC-BY-4.0, canonical legal code in [LICENSE](LICENSE). Copyright (c) 2026 hyderhusainarastu. Each repo in this catalog carries its own LICENSE file.

Keywords: templates, checklists, incident runbook, launch checklist, talk preflight, project scaffold, AGENTS.md, prompt templates.

Part of the palimnote-templates catalog. Hub: [hyderhusainarastu/hyderhusainarastu](https://github.com/hyderhusainarastu/hyderhusainarastu).
