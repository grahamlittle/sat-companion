# Setup — ChatGPT, Gemini, or any other AI

This path uses **one self-contained file**, [`system-prompt.md`](system-prompt.md). It bundles the coach instructions and all the reference material into a single block, because most general chat assistants cannot look separate files up.

## The honest trade-off

`system-prompt.md` is fairly large (~15 KB / ~2,400 words). That matters:

- **Small "custom instructions" boxes will reject it.** ChatGPT's custom-instructions field, for example, is far too short. Do **not** try to paste it there.
- **Instead, paste it as your first message** in a normal chat. Then send your real question as the second message. The AI keeps it in context for the rest of that conversation.
- You must re-paste it in each **new** conversation, unless your tool has a "custom GPT", "Gem", or saved-prompt feature that can hold a long instruction — in which case put it there once.

If your tool supports uploadable knowledge files (like claude.ai Projects), prefer the `claude-project/` path — it is lighter and you do not re-paste anything.

## Steps

1. Open a new chat in your AI tool.
2. Open [`system-prompt.md`](system-prompt.md), copy the **entire** contents, and paste it as your first message. The AI should acknowledge it is now SAT Companion.
3. Send your real question next: *"Digital SAT Math. Here's a question I got wrong and the answer I picked — help me find my mistake, don't just give the answer."*
4. Check it behaves: it should ask for your attempt or reasoning before explaining, name the content domain, and end with `(SAT Companion — Last Updated: September 2026)`.

## Reducing size (optional)

If your tool truncates long messages, you can trim `system-prompt.md`: keep the top instructions and only the reference sections you need. A student focused only on Math can delete the Reading & Writing detail. The reference sections are clearly marked with `## REFERENCE:` headers.

## A note on language quality

SAT Companion tests English, so it always produces practice content in English — but it can *explain* in your first language. How good those explanations are depends on the AI model you run it on, not on this prompt. Strong general-purpose models explain well across many languages; smaller or older models can be weaker outside English.
