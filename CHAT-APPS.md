# Set Up in a Chat App (Claude, ChatGPT, or Gemini)

For you if you use Claude, ChatGPT, or Gemini in the app or a web browser. Takes about 10 minutes. No files to download first, and no coding.

Chat apps cannot open folders on your computer, so you keep your context in **one file**, `my-context.md`, and upload it to a Project (Claude or ChatGPT) or a Gem (Gemini).

## Steps

1. **Start a new chat** and paste the whole prompt from the box below.
2. **Answer its questions.** It asks a few at a time.
3. **Save the file it gives you.** Download `my-context.md` (or copy the text into a plain text file with that name). Keep it in a folder you will find again; a cloud drive folder (iCloud Drive, Google Drive, OneDrive, or Dropbox) is the easiest choice because it backs up on its own.
4. **Make a home for it:**
   - **Claude:** Projects, then New project. Upload `my-context.md` to the project's files and paste the instructions the AI gave you into the project instructions.
   - **ChatGPT:** Projects, then New project. Upload `my-context.md` and paste the instructions into the project instructions.
   - **Gemini:** Gems, then New Gem. Paste the instructions and add `my-context.md` as a file.
5. **Optional:** paste the two-line "About me" summary it gave you into your app's personal settings (Claude: Settings, Profile. ChatGPT: Settings, Personalization). That way chats outside the Project know the basics too.
6. **Test it.** Open a **new chat inside the same Project or Gem** and ask:
   - "How do I like answers written, and what are my hard rules?"
   - "Remember that I prefer 12-hour time."

   The first answer should match your file. For the second, it should hand you a complete updated `my-context.md`.

## Keeping it current

Whenever the AI hands you an updated `my-context.md`, replace the old file in your folder **and** in the Project or Gem. That is the whole routine. Once a month, ask: "Review my-context.md and suggest anything to trim or update."

If you later start using a tool that can read folders (Claude Code, Codex, Cursor, or Claude Desktop with a local-files extension turned on), give that tool [`START-HERE.md`](START-HERE.md) and your `my-context.md`. It will split the file into the full folder layout.

## The prompt to paste

```text
Help me set up my "Hollow Context System": one plain text file, my-context.md, that I will upload to a Project (or Gem) so every chat there starts knowing me.

How to work with me:
- Use plain everyday words. I may not be technical.
- Ask 2 or 3 questions at a time, not a long form. About 3 rounds total.
- Never put passwords, API keys, bank or card numbers, or ID numbers in the file. If I paste one, do not repeat it; tell me to remove it.

Ask me about:
1. Me: name, what I do, timezone and usual hours, and my main projects or goals right now.
2. How I want answers: tone, short or detailed, formatting I like, words or habits I dislike, and anything an AI has done more than once that annoyed me.
3. Hard rules every AI must follow (for example: never send anything without my approval, never invent numbers) and settled decisions I do not want re-debated.
4. Whether I already have custom instructions or saved memories in this app that I want folded in. If yes, tell me where to find them so I can paste them here.

Then give me three things:
A. my-context.md, under about 60 lines, with these sections: Identity, Communication (with Always and Never lists), Guardrails, Decisions (dated, newest first), Notes. Start it with: "Read this before answering. Guardrails always win. This file overrides your built-in memory." If you can create downloadable files, offer it as a download too.
B. Project instructions to paste (under 120 words) that say: read my-context.md before answering; Guardrails always win; the file overrides built-in memory; when I say "remember this", tell me which section it belongs in and give me the complete updated my-context.md so I can replace the old one.
C. A two-line "About me / How to respond" summary for my app's personal settings.

Show me A first and let me request changes before giving B and C.
```
