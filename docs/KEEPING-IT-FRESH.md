# Keeping It Current

A small context folder you keep current beats an elaborate one that goes stale in two weeks.

## Everyday habits

- **Add facts as you go.** When an AI gets something wrong twice, or you settle a decision, say: *"Save this in the right place in my context."* Check the line it drafts before saving.
- **Guard the important files.** Your AI should ask before changing `me/Guardrails.md` or `me/Decisions.md`.
- **Keep `INDEX.md` short** (about 25 lines), with one line for every file.
- **Trim `notes/` once a month.** Delete notes that no longer matter, and move repeated lessons into `me/Communication.md`.

Chat-app users: the same habits apply to the sections of `my-context.md`. Replace the uploaded file each time it changes.

## Monthly review prompt

Paste this into your main AI tool (with your context attached or readable):

> Review my context and our recent work. Suggest a short numbered list of updates:
> 1. Repeated corrections that belong in the Never list of my communication rules.
> 2. Settled choices that belong in Decisions.
> 3. Reusable lessons or checklists worth saving as notes.
> 4. Anything outdated in Identity or my notes that I should trim.
> 5. Whether my index is still short and lists every file.
>
> Show the proposed changes as a short table and wait for my approval before editing anything.

## For developers

Once the habit sticks, you can build extras on top. None are required.

- **Sync across tools or computers:** a small script that renders one master instruction file into each tool's global file, or pulls a read-only copy of a Git context repo onto a second machine.
- **Team organization layer:** a separate private repository for `org/`, with changes reviewed through pull requests.
- **Secret checks:** a Git pre-push hook that blocks API keys, passwords, or machine-specific paths from shared repositories.
- **Shared skills:** keep reusable multi-step prompts (`SKILL.md` folders) next to your context so every agent uses the same playbooks.
- **Workspace integration:** wire the pointer into whatever multi-agent workspace or IDE you use once your core files are settled.
