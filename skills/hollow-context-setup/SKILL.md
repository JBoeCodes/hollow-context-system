---
name: hollow-context-setup
description: Set up the Hollow Context System, a small plain-Markdown context folder (INDEX.md plus four personal files, a notes folder, and optional computer, project, and team layers) that gives every AI tool the same background, tone, and rules. Use when the user asks to set up, initialize, or organize their AI context, personal instructions, or memory files.
---

# Hollow Context System Setup

Self-contained. The full guide (`START-HERE.md`) and copy-as-is files (`starter/`) live at the Hollow Context System repository if the user has it; use them when available.

## 1. Check what you can do

- **Cannot read and write files on the user's computer** (chat app or browser): build one file, `my-context.md` (sections: Identity, Communication with Always and Never lists, Guardrails, Decisions, Notes; under about 60 lines). Then give Project instructions telling the app to read it first, follow Guardrails first, and hand back the complete updated file whenever the user says "remember this." The user uploads it to a Claude or ChatGPT Project or a Gemini Gem and tests in a new chat inside that same Project.
- **Can read and write files:** continue below.

## 2. Interview (2 or 3 questions at a time, plain words)

1. Which AI tools they use. 2. Where to keep the folder: most people a cloud drive folder set to available offline; Git users a private repository outside any cloud-synced folder (check whether `Documents` is synced by iCloud or OneDrive first); otherwise `~/AI-Context`. 3. Name, role, timezone, current focus. 4. Tone, length, dislikes, repeated annoyances. 5. Hard rules and settled decisions. 6. Existing instructions in other tools (read only with permission; confirm before reusing).

## 3. Create the folder (show drafts first)

```text
INDEX.md            about 25 lines; one line per file with a "Load:" trigger
me/Identity.md      who they are, current focus
me/Communication.md tone, length, Always and Never (dated stop-habits go under Never)
me/Guardrails.md    hard rules; always win
me/Decisions.md     settled choices, newest first
notes/              one short file per fact, lesson, or checklist
home/<computer>.md  optional, under about 40 lines
```

Put this priority rule at the top of `INDEX.md`: Guardrails always win; project rules override personal style inside that project; these files override built-in app memory; ask if still unclear.

## 4. Connect tools

Save a short pointer (folder path, read `INDEX.md` then only needed files, the priority rule, the placement test below, ask before editing Guardrails or Decisions, never store secrets) in each tool's global instructions: Claude Code `~/.claude/CLAUDE.md` (also add `@<path>/INDEX.md`), Codex `~/.codex/AGENTS.md`, Gemini CLI `~/.gemini/GEMINI.md`, Cursor User Rules. For other tools, look up current docs and confirm with the user. Back up existing files as `<name>.bak-<YYYY-MM-DD>`. Quote paths with spaces.

Placement test (stop at first yes): only this computer, Home; only one project, that project's `AGENTS.md`; whole team, Organization (suggest, do not edit); otherwise Personal.

## 5. Test in a new chat or session

Ask: "How do I like answers written, and what are my hard rules?", "What am I focused on?", and "Remember that I prefer 12-hour time." Answers should cite the files; the last should land in `me/Communication.md` after approval.

## Always

- Never edit the starter repository itself; create the user's folder elsewhere.
- Never write passwords, API keys, tokens, account or ID numbers, or private HR data. If the user pastes one, do not repeat it.
- Git repositories are private by default.
