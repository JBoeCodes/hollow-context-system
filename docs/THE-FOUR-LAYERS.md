# The Four Layers

Every kind of fact gets **one clear home**. Create only the layers you need; most people only need Personal.

| Layer | What belongs here | Examples | Who needs it |
|---|---|---|---|
| **Personal** (`me/`, `notes/`) | Who you are, how you want answers written, hard rules, settled decisions, short notes | "Keep replies under 5 bullets", "Never send email without my approval" | Everyone |
| **Home** (`home/<computer>.md`) | Facts true only on one computer | Where folders live on this laptop, installed apps, quirks | Optional |
| **Project** (`AGENTS.md` in a project folder) | Rules for one project | Goals, audience, tone for that project, past gotchas | Optional |
| **Organization** (`org/`) | Facts shared by a whole team or company | Glossary, who owns what, shared rules | Optional |

The Personal layer is four files plus one folder:

- `me/Identity.md`: who you are and what you are focused on.
- `me/Communication.md`: tone, length, and Always / Never lists. Habits you want an AI to stop go under Never, with the date.
- `me/Guardrails.md`: hard rules that override everything.
- `me/Decisions.md`: settled choices, newest first.
- `notes/`: one short file per remembered fact, lesson, or checklist.

Split any file further once it grows past a page.

## Where a new fact goes

Ask in order and stop at the first **yes**:

1. Only true on this one computer? **Home.**
2. Only true for one project, even if it is about how you like things done there? **Project.**
3. True for everyone on my team or company? **Organization.**
4. Otherwise it is about me: **Personal.**

Use the narrowest layer that is true. Link to shared facts instead of copying them into personal files.

## Which rule wins

1. `me/Guardrails.md` always wins.
2. Inside a project, that project's rules override your personal style. ("Formal tone with contractors on the kitchen remodel" beats "casual tone" while working on the remodel.)
3. Your files override any AI app's built-in memory.
4. If it is still unclear, the AI asks you.

## Why `INDEX.md` stays short

Pasting a huge document into every chat wastes space and makes the AI miss the rules that matter. Instead, `INDEX.md` (about 25 lines) lists each file with one line on what it holds and when to read it:

```markdown
- `me/Communication.md`: tone, length, always/never rules. Load: before writing messages or docs.
- `me/Guardrails.md`: hard rules. Load: before outside actions or big decisions.
```

At the start of a task, an AI that can read files opens `INDEX.md` and then only the one or two files it needs. Chat apps that cannot open folders use one combined file instead (see [`CHAT-APPS.md`](../CHAT-APPS.md)).

## What never goes in a context folder

- **Secrets:** passwords, API keys, tokens, bank or card details.
- **Sensitive personal or HR data:** ID numbers, pay, medical or disciplinary records, private details about other people.
- **Large files:** spreadsheets, PDFs, archives, media. Link to where they live instead.
- **Day-to-day to-do lists:** those belong in a task app.
- **Long manuals:** keep files to about a page; put deep reference material in the project it belongs to.

## Quick examples

| Fact | Layer | File |
|---|---|---|
| "Write concise replies; skip filler intros" | Personal | `me/Communication.md` |
| "Stop inventing numbers when data is missing" (second time it happened) | Personal | `me/Communication.md` (Never) |
| "Never send an email without showing me first" | Personal | `me/Guardrails.md` |
| "We stay on Notion (decided May 2026)" | Personal | `me/Decisions.md` |
| "Checklist I use before publishing a newsletter" | Personal | `notes/newsletter-checklist.md` |
| "My context folder is in `Google Drive/AI-Context`" | Home | `home/my-computer.md` |
| "Formal tone with contractors on the kitchen remodel" | Project | `kitchen-remodel/AGENTS.md` |
| "Run tests with `npm test`" | Project | `<repo>/AGENTS.md` |
| "Company acronyms and who owns what" | Organization | `org/glossary.md` |
