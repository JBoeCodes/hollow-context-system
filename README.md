# Hollow Context System

Give any AI assistant the same background about you, your work, and your preferences, without getting locked into one app.

It is a small folder of plain text files. No code, no special software, and no GitHub account needed.

## Get started

- **Using Claude, ChatGPT, or Gemini in an app or browser?** Open [`CHAT-APPS.md`](CHAT-APPS.md), copy the prompt at the bottom into a new chat, and follow the six steps. About 10 minutes.
- **Using an AI that can work with files on your computer** (Claude Code, Codex, Cursor, Gemini CLI, Antigravity, or Claude Desktop with a local-files extension)? Give it this folder or [`START-HERE.md`](START-HERE.md) and say:
  > Follow START-HERE.md and set up my Hollow Context System.

The AI asks a few plain-English questions, drafts your files for you to approve, and shows you how to connect the tools you use.

> **For AI assistants:** If a user gave you this repository and asked you to set it up, do not summarize this page. Open [`START-HERE.md`](START-HERE.md) and begin. Create the user's files in a separate location they choose; never edit files inside this repository.

## How it works

Every fact gets one home, in up to four layers. Most people only need the first.

| Layer | What goes here | Needed? |
|---|---|---|
| **Personal** (`me/`, `notes/`) | Who you are, how you want answers written, hard rules, settled decisions, short notes | Yes |
| **Home** (`home/<computer>.md`) | Facts true only on one computer | Optional |
| **Project** (`AGENTS.md` in a project folder) | Rules for one project | Optional |
| **Organization** (`org/`) | Facts shared by your whole team or company | Optional |

A short table of contents, `INDEX.md` (about 25 lines), tells the AI what each file holds, so it reads only what the current task needs.

**Where does a new fact go?** Stop at the first yes: only true on this computer (Home); only true for one project (Project); true for my whole team (Organization); otherwise it is about me (Personal).

**Which rule wins?** Your Guardrails always win. Inside a project, project rules beat your personal style. Your files beat any app's built-in memory.

## What is in this folder

- [`CHAT-APPS.md`](CHAT-APPS.md): one-page setup for Claude, ChatGPT, and Gemini apps, with a paste-and-go prompt.
- [`START-HERE.md`](START-HERE.md): full setup guide for AI tools that can read and write files.
- [`starter/`](starter/): the blank folder to copy as is.
- [`extras/`](extras/): optional files for a computer, a project, a team, and tool instructions.
- [`examples/`](examples/): a filled-in example for a fictional operations manager.
- [`docs/`](docs/): short guides on [the four layers](docs/THE-FOUR-LAYERS.md), [where to store your files](docs/STORAGE-OPTIONS.md), [connecting tools](docs/CONNECTING-TOOLS.md), and [keeping it current](docs/KEEPING-IT-FRESH.md).

## For developers

- Works with any model (plain Markdown), any agent harness or IDE (one pointer file per tool), and any workspace manager. No daemons, scripts, or sync machinery.
- [`skills/hollow-context-setup/`](skills/hollow-context-setup/SKILL.md) is a self-contained Agent Skill you can copy into `~/.claude/skills/` or `~/.agents/skills/`.
- Ideas for adding sync, team review, and secret checks on top: [`docs/KEEPING-IT-FRESH.md`](docs/KEEPING-IT-FRESH.md#for-developers).

## License

MIT. See [`LICENSE`](LICENSE).
