# Connecting Your AI Tools

Each AI tool has one place for standing instructions. Point it at your context with the lightest method it supports. Back up any existing instruction file first (for example `CLAUDE.md.bak-2026-11-21`).

## Chat apps (Claude, ChatGPT, Gemini)

Chat apps cannot open folders on your computer. Follow [`CHAT-APPS.md`](../CHAT-APPS.md): keep one `my-context.md`, upload it to a Project (Claude or ChatGPT) or a Gem (Gemini), and paste [`extras/pointers/chat-app-instructions.md`](../extras/pointers/chat-app-instructions.md) into the instructions.

- **Updating:** when the AI hands you an updated file, replace it in your folder and in the Project or Gem.
- **Testing:** start a new chat **inside the same Project or Gem**. Chats outside it will not see the file.
- **Built-in memory:** keep lasting facts in your file rather than the app's memory feature so you can take them to any AI. Your file wins if they disagree.

**Claude Desktop with local files:** if you turn on a local-files extension or connector and allow your context folder, Claude Desktop can read the folder directly. Put the tool pointer below in your Project instructions instead of uploading files.

## Tools that read files on your computer

Fill in [`extras/pointers/agent-tool-pointer.md`](../extras/pointers/agent-tool-pointer.md) with your real folder path (in quotes if it has spaces) and save it here:

| Tool | Where the pointer goes | Per-project file |
|---|---|---|
| Claude Code | `~/.claude/CLAUDE.md`, plus the line `@<PATH_TO_CONTEXT>/INDEX.md` so the index loads on its own | `CLAUDE.md` (can be the one line `@AGENTS.md`) |
| Codex | `~/.codex/AGENTS.md` | `AGENTS.md` |
| Gemini CLI | `~/.gemini/GEMINI.md` | `GEMINI.md` or `AGENTS.md` |
| Antigravity | `~/.gemini/config/GEMINI.md` | `AGENTS.md` |
| Cursor | Settings, Rules, User Rules (paste the text) | `AGENTS.md` or `.cursor/rules/` |

Locations checked November 2026. Tools move these settings; for any tool not listed, or if a path no longer works, ask your AI to look up the tool's current documentation for "global instructions" or "user rules."

**If the tool will not read your context folder:** some tools stay inside the project you opened. Approve the read when asked, or add the context folder to the tool's allowed folders. In Claude Code the `@` line above avoids the problem.

## One file for every coding tool in a project

If you use more than one coding tool on the same project, keep project instructions in `AGENTS.md` and make `CLAUDE.md` the single line:

```markdown
@AGENTS.md
```
