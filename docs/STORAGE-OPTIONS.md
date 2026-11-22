# Where to Keep Your Files

Your context is a small folder of plain text files. You can move it later by copying the folder.

## Pick one

| You are... | Keep it in | Example |
|---|---|---|
| Most people | A cloud drive folder (iCloud Drive, Google Drive, OneDrive, or Dropbox) | `Google Drive/AI-Context/` |
| A developer who already uses Git | A **private** Git repository outside any cloud-synced folder | `~/repos/personal-context` |
| Someone who wants no cloud and no Git | A plain folder in your home folder | `~/AI-Context` |

**Cloud drive folder.** Backs up on its own, works on your phone and other computers, and makes uploading to Claude, ChatGPT, or Gemini easy. Editing the same file on two devices at the same moment can create a "conflicted copy"; delete the older one.

**Private Git repository.** Full change history and team review through pull requests. Always private, never public.

**Plain folder.** Works offline with nothing to sign into. Back it up the way you back up everything else.

## Two things to check

1. **Keep the folder available offline.** Cloud drives can keep files "online only" to save space, and AI tools cannot read those. Right-click the folder and choose "Keep Downloaded" (iCloud), "Always keep on this device" (OneDrive), or "Available offline" (Google Drive). Dropbox: "Make available offline."
2. **Never put a Git repository inside a cloud-synced folder.** Cloud sync and Git fight over the same files and can corrupt the repository. Watch for folders that are synced without you noticing: on many Macs, `Documents` and `Desktop` sync to iCloud, and on many Windows PCs, `Documents` syncs to OneDrive. A Git repository belongs somewhere like `~/repos/`.

Cloud folder names often contain spaces (`Google Drive`, `Mobile Documents`). When a tool or instruction file needs the path, put it in quotes.

## Chat apps only?

If you only use Claude, ChatGPT, or Gemini in an app or browser, you keep one file, `my-context.md`. Put it in a cloud drive folder so you can find and re-upload it from any device. See [`CHAT-APPS.md`](../CHAT-APPS.md).
