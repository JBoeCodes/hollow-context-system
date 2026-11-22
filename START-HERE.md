# Hollow Context System: Start Here

**Using Claude, ChatGPT, or Gemini in a chat app or browser?** Use [`CHAT-APPS.md`](CHAT-APPS.md) instead. It is shorter and built for apps that cannot open folders.

**Using an AI that can read and write files on your computer** (Claude Code, Codex, Cursor, Gemini CLI, Antigravity, Claude Desktop with a local-files extension, or similar)? Give it this file, or this whole folder, and say:

> Follow START-HERE.md and set up my Hollow Context System.

Setup takes about 10 minutes.

---

## Instructions for the AI assistant

You are helping one person set up a **Hollow Context System**: a small folder of plain Markdown files that gives every AI tool they use the same background, tone, and rules.

**First, check what you can do.** If you cannot read and write files on the user's computer, stop here and follow the chat-app flow instead: use [`CHAT-APPS.md`](CHAT-APPS.md) if you have it; otherwise interview the user (Step 2, Batch B) and produce one `my-context.md` file (sections: Identity, Communication, Guardrails, Decisions, Notes; under about 60 lines) plus short Project instructions telling the app to read that file, follow its Guardrails first, and hand back the complete updated file whenever the user says "remember this."

Operating rules for the whole setup:
- **Match the user's comfort level.** Do not assume they know Git, GitHub, Markdown, or terminal commands. Use plain words unless they say they are a developer.
- **Never edit files inside this starter repository.** Create the user's folder in a separate location they choose.
- **Use the rest of the repository if you have it.** Copy [`starter/`](starter/) as is, use [`extras/`](extras/) for optional layers, and match the brevity of [`examples/`](examples/).
- **Ask 2 or 3 questions at a time.** Never a long form.
- **Show drafts before writing or replacing anything.** Before replacing an existing instruction file, back it up as `<filename>.bak-<YYYY-MM-DD>`.
- **Never store secrets.** No passwords, API keys, tokens, bank or card numbers, ID numbers, or private HR or pay records. If the user pastes one, do not repeat it; tell them to remove or change it.

---

### Step 1: Explain the idea (30 seconds)

In plain words:
- Instead of repeating yourself in every chat, or locking your preferences inside one AI app's memory, you keep a small folder of text files that any AI can read.
- A short table of contents, **`INDEX.md`** (about 25 lines), tells the AI what each file holds and when to read it, so it opens only what the current task needs.
- Facts live in up to four layers. Create only the ones the user needs:
  1. **Personal (`me/` and `notes/`):** who you are, how you want answers written, hard rules, settled decisions, and short notes. Everyone starts here.
  2. **Home (`home/<computer>.md`):** facts true only on one computer. Optional.
  3. **Project (`AGENTS.md` inside a project folder):** rules for one project. Optional.
  4. **Organization (`org/`):** facts shared by a whole team or company. Optional.

Where a new fact goes (stop at the first yes):
1. Only true on this one computer? **Home.**
2. Only true for one project (even if it is about how you like things done there)? **Project.**
3. True for everyone on my team or company? **Organization.**
4. Otherwise it is about me: **Personal.**

Which rule wins when two disagree:
1. `me/Guardrails.md` always wins.
2. Inside a project, the project's rules override personal style.
3. The files override any AI app's built-in memory.
4. If it is still unclear, ask.

---

### Step 2: Short interview (about 3 turns)

**Batch A: tools and storage**
1. Which AI tools do you use, and which one most?
2. Where should the folder live? Recommend one default instead of a menu:
   - **Most people: a cloud drive folder** (iCloud Drive, Google Drive, OneDrive, or Dropbox), for example `Google Drive/AI-Context/`. It backs up on its own and is easy to upload from. Look for which cloud folders actually exist before proposing a path (macOS: `~/Library/Mobile Documents/com~apple~CloudDocs/` for iCloud Drive and `~/Library/CloudStorage/` for others; Windows: folders under the user's home such as `OneDrive`). Then have the user mark the folder **available offline** ("Keep Downloaded" in iCloud, "Always keep on this device" in OneDrive, "Available offline" in Google Drive), because AI tools cannot read files that live only in the cloud.
   - **Developers who already use Git:** a **private** Git repository kept outside any cloud-synced folder, for example `~/repos/personal-context`.
   - **No cloud and no Git:** a plain folder in the user's home folder, for example `~/AI-Context`.
3. Is this just for you, or will a team share some of it later?

Storage checks before you write anything:
- **Never put a Git repository inside a cloud-synced folder.** On many Macs, `Documents` and `Desktop` are synced by iCloud, and on many Windows PCs `Documents` is synced by OneDrive. Check before placing a Git repository there.
- **Paths with spaces** (common in cloud folders, such as `Google Drive`): wrap them in quotes in every command and pointer file.

**Batch B: about you**
4. Your name, what you do, timezone, and the main projects or goals on your plate.
5. How should AI respond? Tone, length, formatting, words you dislike, and anything an AI has done more than once that annoyed you.
6. Hard rules every AI must follow, and settled decisions you do not want re-debated.

**Batch C: what you already have**
7. Do you already have custom instructions or saved memories in another AI tool? With the user's permission, read existing files without changing them (for example `~/.claude/CLAUDE.md`, `~/.codex/AGENTS.md`, `~/.gemini/GEMINI.md`). For chat apps, tell them where to copy from (Claude: Settings, Profile. ChatGPT: Settings, Personalization). Show a short table (`Item | Where it came from | Proposed file`) and confirm before using any of it.
8. Only if it fits their tools: offer a `home/<computer>.md` file or a starter project `AGENTS.md`.

---

### Step 3: Create the folder

1. Copy [`starter/`](starter/) to the chosen location as is (or use Appendix A if you only have this file). Fill in each `<angle bracket>` from the interview and delete anything left unused.
2. Add optional files from [`extras/`](extras/) only if the user wants them (`home/`, `project/`, `org/`), and add one line for each to `INDEX.md`.
3. Keep it short: `INDEX.md` about 25 lines, each `me/` file under one page, `home/<computer>.md` under about 40 lines.
4. Show the drafts, apply the user's changes, then write the files.
5. If the user chose Git: create a **private** repository (never public) and commit the files. Do not add sync scripts or automation unless they ask.

Remind the user what stays out: passwords and keys, account and ID numbers, other people's private or HR information, large files (spreadsheets, PDFs, archives), and day-to-day to-do lists.

---

### Step 4: Connect their tools

Set up only the tools the user actually uses. Fill in Appendix B (or [`extras/pointers/agent-tool-pointer.md`](extras/pointers/agent-tool-pointer.md)) with the real folder path and save it where the tool reads global instructions. Back up any existing file first.

| Tool | Where the pointer goes |
|---|---|
| Claude Code | `~/.claude/CLAUDE.md`. Also add the line `@<PATH_TO_CONTEXT>/INDEX.md` so the index loads on its own. |
| Codex | `~/.codex/AGENTS.md` |
| Gemini CLI | `~/.gemini/GEMINI.md` |
| Antigravity | `~/.gemini/config/GEMINI.md` |
| Cursor | Settings, Rules, User Rules (paste the text) |
| Claude Desktop | Turn on a local-files extension or connector and allow the context folder, then put the pointer in your Project instructions. Without it, use [`CHAT-APPS.md`](CHAT-APPS.md). |
| Anything else | Look up the tool's current documentation for its global or user instructions file, and confirm the location with the user before writing. |

Tools that stay inside a project folder may block reading the context folder. If that happens, approve the read when asked, or add the context folder to the tool's allowed folders. For Claude Code, the `@` line above avoids the problem.

For chat apps the user also uses, follow [`CHAT-APPS.md`](CHAT-APPS.md) (upload the files to a Project and paste [`extras/pointers/chat-app-instructions.md`](extras/pointers/chat-app-instructions.md)).

---

### Step 5: Test it (2 minutes)

Have the user open a **brand-new chat or session** in their main tool and ask:

1. "How do I like answers written, and what are my hard rules?"
2. "What am I focused on right now?"
3. "Remember that I prefer 12-hour time."

The first two answers should come from their files, naming the file used. For the third, the AI should pick `me/Communication.md`, show the line, and save it after approval. Fix any gap, then give a short recap: where the folder lives, how to add a fact ("save this in the right place in my context"), and the monthly habit of trimming `notes/`.

---

## Appendix A: Starter files (same as `starter/`)

Use these only if you do not have the `starter/` folder.

### `INDEX.md`

```markdown
# Context Index

One line per file: what it holds and when to read it. Read only what the task needs. Keep this file short (about 25 lines).

## Rules of priority
- `me/Guardrails.md` always wins.
- Inside a project, that project's `AGENTS.md` overrides my personal style.
- These files override any AI app's built-in memory. If two rules conflict and none of the above settles it, ask me.

## About me (`me/`)
- `me/Identity.md`: who I am, role, timezone, current focus. Load: for background on me.
- `me/Communication.md`: tone, length, formatting, always/never rules. Load: before writing any answer, message, or document.
- `me/Guardrails.md`: hard rules. Load: before any outside action, draft, or big decision.
- `me/Decisions.md`: settled choices not to reopen. Load: before suggesting a change of direction or tools.

## Notes (`notes/`)
- `notes/`: one short file per remembered fact, lesson, or checklist. Load: when a filename matches the task.

## Optional (delete lines you do not use)
- `home/my-computer.md`: folders, apps, and quirks on this computer. Load: when a task touches local files or setup.
```

### `me/Identity.md`

```markdown
# Identity

- **Name:** <your name>
- **What I do:** <role, work, or main focus>
- **Timezone and usual hours:** <timezone and hours>

## Current focus

- <one line per current priority or project>

## Helpful background

- <tools you use, responsibilities, or anything you are tired of repeating>
```

### `me/Communication.md`

```markdown
# Communication

- **Tone:** <e.g. plain, direct, friendly, formal>
- **Default length:** <e.g. short and scannable; longer only when I ask>

## Always

- <habits you want in every reply>

## Never

- <words, formats, or habits you dislike>
- <YYYY-MM-DD: anything an AI did twice that you want it to stop doing>
```

### `me/Guardrails.md`

```markdown
# Guardrails

Hard rules that always apply and override everything else. Ask me before changing this file.

- Never write passwords, API keys, tokens, or sensitive personal numbers into any file.
- Never send emails or outside messages for me without my approval of the exact text.
- <your own hard rules>
```

### `me/Decisions.md`

```markdown
# Decisions

Settled choices, newest first. Treat these as decided. Ask me before reopening or changing any of them.

## <YYYY-MM-DD>: <short title>

- <what was decided, and the one-line reason>
```

---

## Appendix B: Pointer for tools that read files

Same as [`extras/pointers/agent-tool-pointer.md`](extras/pointers/agent-tool-pointer.md). Replace `<PATH_TO_CONTEXT>` with the real folder path.

```markdown
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
```
