# hollow-context-system

A minimal, model-agnostic, harness-agnostic starter for the Hollow Context System, usable by non-technical chat-app users and by coding agents.

## If a user gave you this repository to set up their context

1. **Do not summarize this repo and stop.** Follow [`START-HERE.md`](START-HERE.md) from the top. If you cannot read and write files on the user's computer, follow [`CHAT-APPS.md`](CHAT-APPS.md) instead.
2. **Never edit files inside this starter repository.** Create the user's context in a separate location they choose.
3. Copy [`starter/`](starter/) as is, use [`extras/`](extras/) for optional layers, and match the brevity of [`examples/`](examples/README.md).

## Layout

- `README.md`: plain-English overview and routing.
- `CHAT-APPS.md`: one-page chat-app setup (single `my-context.md` file) with a paste-and-go prompt.
- `START-HERE.md`: full setup guide for file-capable agents, with inline copies of `starter/` (Appendix A) and the agent pointer (Appendix B).
- `starter/`: copy-as-is personal layer (`INDEX.md`, four `me/` files, `notes/`).
- `extras/`: optional `home/`, `project/`, `org/`, and `pointers/`.
- `examples/`: one fictional filled-in folder, plus the same facts as a single `my-context.md`.
- `docs/`: `THE-FOUR-LAYERS.md`, `STORAGE-OPTIONS.md`, `CONNECTING-TOOLS.md`, `KEEPING-IT-FRESH.md`, `BUILD_LOG.md`.
- `skills/hollow-context-setup/SKILL.md`: self-contained Agent Skill (no links outside its folder).

## Maintaining this repository

- Pure Markdown. No required scripts, Git, terminal, sync machinery, or vendor or composer lock-in.
- Zero personal data, company facts, or secrets. No references to the maintainer's own tools or workspace.
- Single sources, kept in sync on every edit:
  - `starter/` files must match `START-HERE.md` Appendix A exactly.
  - `extras/pointers/agent-tool-pointer.md` (minus its comment line) must match Appendix B.
  - The placement test and priority rule must read the same in `README.md`, `START-HERE.md`, `docs/THE-FOUR-LAYERS.md`, the pointers, and the skill.
  - The tool table lives in `START-HERE.md` Step 4 and `docs/CONNECTING-TOOLS.md`; only list paths that were checked, and date the check.
- Keep every `INDEX.md` under 2,048 bytes. User-facing copy says "about 25 lines", never byte counts.
- Never add GitHub Actions workflows.
- Update `docs/BUILD_LOG.md` on every substantive change.
