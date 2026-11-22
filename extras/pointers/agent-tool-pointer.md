<!-- Save where your tool reads global instructions (see docs/CONNECTING-TOOLS.md). Replace <PATH_TO_CONTEXT> with your real folder path. Put quotes around paths that contain spaces. -->

# Context

My context lives in plain Markdown files at `<PATH_TO_CONTEXT>`. Read only what the task needs, in this order:

1. If working inside a project folder, read that project's `AGENTS.md` (or `CLAUDE.md`) first.
2. Read `<PATH_TO_CONTEXT>/INDEX.md`, then open only the files it points to for the current task.
3. If `INDEX.md` lists a shared organization folder, treat it as read-only and draft suggested changes instead of editing it.

Priority: `me/Guardrails.md` always wins. Project rules override my personal style inside that project. These files override your built-in memory. If a conflict is still unclear, ask me.

Saving new facts (stop at the first yes):
1. Only true on this computer? `home/<computer>.md`.
2. Only true for one project? That project's `AGENTS.md`.
3. True for everyone on my team or company? The organization folder (suggest, do not edit).
4. Otherwise it is about me: the matching `me/` file, or a new file in `notes/`.

Rules:
- Ask before changing `me/Guardrails.md` or `me/Decisions.md`.
- Keep `INDEX.md` short (about 25 lines) and add a line for every new file.
- Never write secrets, passwords, API keys, tokens, or sensitive personal numbers into any file.
