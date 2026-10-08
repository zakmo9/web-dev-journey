# 🔗 REFERENCE PROTOCOL — Refer to any point in any lesson

Use this to ask me to explain **anything from any lesson**, and I'll connect it to **the current lesson**.

## The keyword

| Command | What it does |
|---|---|
| **`reference <chapter> <topic>`** | Tells me to look up `<chapter>` and `<topic>`, explain it, and **connect it to the current lesson**. |

## Format

```
reference <chapter-number> <topic-keyword>
```

- `<chapter-number>` = the lesson number (e.g., `1`, `2`)
- `<topic-keyword>` = a word from that lesson's topics (e.g., `css`, `git`, `flex`, `responsive`)

## Examples

```
You: "reference 1 nodejs"
Me: "Node.js is... This connects to Lesson 2 because..."

You: "reference 2 responsive"
Me: "Responsive design is... In our current Lesson 2, we use @media to..."

You: "reference 1 git"
Me: "Git is... We'll use this in Lesson 3 to save our landing page..."
```

## How it works

1. You say `reference <chapter> <topic>`.
2. I look up `<chapter>` and `<topic>` in `references.json`.
3. I explain the topic **in simple terms** (like explaining to a 10-year-old).
4. I then **connect it to the current lesson** — showing how it relates to what you're learning right now.
5. **The lesson state does NOT change.** You stay on the same lesson.

## What gets saved

Every reference request is logged in `references.json` under `lastReference`:

```json
{
  "lastReference": {
    "at": "2026-10-05T14:07:41Z",
    "chapter": "2",
    "topic": "responsive",
    "currentLesson": 2
  }
}
```

## Important rules

- **The lesson never moves during a reference.** `currentLesson` stays exactly where it was.
- **Your questions never advance the lesson.** Only an explicit "continue" or "next lesson" does.
- **You can reference any chapter, even future ones** (I'll explain what's coming and how it connects).
- **The reference index is saved on disk**, so even after a reboot, the index is intact.

## Quick resume after a reboot

1. Open `C:\Users\hp\Documents(web-dev-journey` in VS Code.
2. Look at `references.json` — it shows all available chapters and topics.
3. Type `reference <chapter> <topic>` to ask about anything.

## Combining with WAIT and CONTINUE

- Say `reference ...` → I explain and connect. Lesson unchanged.
- Say `wait` → I pause mid-response.
- Say `pass on` → I resume from where I was interrupted.
- Say `continue` → I advance the lesson.

All three systems work together without interfering.