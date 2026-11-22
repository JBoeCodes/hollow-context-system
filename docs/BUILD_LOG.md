# Build log

Newest entry on top. Format: date, what changed, why, how verified.

## 2026-11-21: Apply second-opinion review (HOL-102)

- **What changed:**
  - Added `CHAT-APPS.md`: a one-page chat-app path (single `my-context.md`, Project or Gem upload, full-file update loop, test inside the same Project) with a paste-and-go prompt. `START-HERE.md` now routes chat-app users there and is cut from 16.7 KB to a file-capable agent guide.
  - Replaced `templates/` with copy-as-is `starter/` (`INDEX.md`, four `me/` files, `notes/`) and `extras/` (`home/`, `project/`, `org/`, `pointers/`). `START-HERE.md` Appendix A and B now mirror these files exactly.
  - Simplified the personal layer to four files plus `notes/`: `Anti-patterns.md` folds into the Never list of `Communication.md`, and `memory/` plus `learnings/` merge into `notes/`.
  - Added a priority rule (Guardrails win; project rules override personal style inside a project; files override built-in app memory; ask if unclear) and reordered the placement test to Home, Project, Organization, Personal.
  - Storage: one recommended default per user type, "available offline" instructions for cloud drives, warnings about silently synced `Documents` folders and paths with spaces.
  - Tools: short checked list (Claude Code with `@` import, Codex, Gemini CLI, Antigravity, Cursor User Rules, Claude Desktop local-files extension) plus a "look up current docs" rule; note on tools that block reading outside the project.
  - Made the skill self-contained, moved developer jargon under "For developers", replaced byte counts with "about 25 lines" in user copy, and added `examples/notes/`, a sample project `AGENTS.md`, and a single-file `examples/my-context.md`. New verification test: "Remember that I prefer 12-hour time."
- **Why:** The review found the repo worked for coding agents but not for non-technical chat-app users, and that duplicated templates had already drifted.
- **How verified:** Checked that `starter/` matches Appendix A and the pointer matches Appendix B, every internal link resolves, all `INDEX.md` files are under 2,048 bytes, and there are no em or en dashes and no references to the maintainer's own tools.

## 2026-11-21: Tighten agent handoff directives in AGENTS.md, README.md, and START-HERE.md

- **What changed:**
  - Added top-of-file setup routing in `AGENTS.md` and a direct "For AI assistants" callout in `README.md` instructing any agent handed the repo or URL to immediately open `START-HERE.md`, start Step 1, and create the user's files in a separate location without editing the template repo.
  - Updated `START-HERE.md` so agents with repo access calibrate brevity against `examples/`, inspect real cloud-drive mount paths (including macOS iCloud Drive / `~/Library/CloudStorage/`) before guessing paths, and offer downloadable files or a `.zip` archive in chat/desktop apps when supported.
- **Why:** Ensure handing the repository URL or clone directly to any coding agent or desktop chat app kicks off clean end-to-end setup on the first try instead of summarizing the README or editing template files in place.
- **How verified:** Checked for em and en dashes, personal or company leaks, broken internal links, and `INDEX.md` byte budgets (all clean).

## 2026-11-21: Simplify repository to a minimal, universal, zero-code starter

- **What changed:**
  - Replaced the script-heavy, multi-machine, workspace-coupled initial scaffold (76 files) with a lean, pure-Markdown starter repository (~28 files) centered on a single self-contained entry point (`START-HERE.md`).
  - Removed bundled Python sync, init, and scanner tools, OS schedulers, and workspace-manager wiring so anyone (including non-technical Claude Desktop and ChatGPT Desktop users with no GitHub or coding background) can drop `START-HERE.md` into any AI and start in 5 minutes using a local folder, cloud drive (iCloud/Google Drive/OneDrive/Dropbox), or private Git repo.
  - Added plain-English guides (`docs/THE-FOUR-LAYERS.md`, `docs/STORAGE-OPTIONS.md`, `docs/CONNECTING-TOOLS.md`, `docs/KEEPING-IT-FRESH.md`), minimal `templates/`, a complete filled-in fictional example (`examples/`), and a lightweight `skills/hollow-context-setup/SKILL.md`.
- **Why:** Keep the Hollow Context System minimal, approachable for non-coders and developers alike, and free of opinionated syncing/multi-machine/composer machinery so users can grow their own workflows on top.
- **How verified:** Verified all `INDEX.md` files under 2,048 bytes, all internal Markdown links resolve cleanly, zero em/en dashes, zero personal or company leaks, and zero GitHub Actions workflows.

## 2026-11-21: Initial repository creation

- **What changed:** Created initial `hollow-context-system` repository with four-layer docs, templates, and tooling.
- **Why:** Package the Hollow Context System for sharing.
- **How verified:** Initial unit tests and leak checks passed prior to simplification.
