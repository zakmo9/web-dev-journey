# 🐾 Web Dev Journey

A complete, step‑by‑step journey to build a real‑time web + mobile app with JavaScript, HTML, CSS, Git, and GitHub — from scratch to professional.

---

## How to resume ANY time

1. Open this folder in VS Code (or any file explorer).
2. **I will read `state.json` automatically** — it holds the exact current lesson, progress, and the latest confirmation question.
3. Tell me **"continue"** — I’ll read `state.json` and pick up where we left off.
4. **Homework confirmation:** After each lesson I **will always ask** "Have you completed the homework for Lesson N? Reply `yes` or `no`." You must answer `yes` before the lesson advances. (See **`CONFIRMATION_PROTOCOL.md`** for details.)

---

## Current checkpoint

- **Lesson** (from `state.json` → `currentLesson` → `currentLessonTitle`)
- **Progress** (from `state.json` → `inProgress.lastAction`)
- **Homework status** (`inProgress.homeworkDone`)

---

## Folder map

```
web-dev-journey/
├── README.md            <- this file
├── SETUP_GUIDE.md       <- detailed tool‑install & checklist
├── CONFIRMATION_PROTOCOL.md <- how lessons are confirmed
├── WAIT_PROTOCOL.md      <- pause / resume instructions
├── REFERENCE_PROTOCOL.md <- how to ask about any topic
├── state.json           <- master progress tracker (read/write)
├── control.json         <- wait / pass‑on state
├── references.json      <- searchable index for 'reference' queries
├── lessons/             <- each lesson is a short .md file
│   ├── 01-setup.md
│   ├── 02-html-css-landing.md
│   └── ...
└── src/                 <- the live website code
    ├── index.html
    ├── style.css
    └── ...
```

---

## Current lesson

See `state.json` → `currentLesson`.

## Next steps

1. **Set up** everything using `SETUP_GUIDE.md`.
2. When ready, reply **`yes`** to the confirmation question (I will ask it right after the next lesson is taught).
3. I’ll mark the lesson complete and advance to the next lesson.
4. Use `continue` to stay on the same lesson, `wait` / `pass on` to pause, or `reference <chapter> <topic>` for help.