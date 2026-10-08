# SETUP GUIDE — Web Development Journey

This guide ensures both of us are on the same page before we start the lessons. Follow each step, then tell me **`yes`** when you’re done. I’ll only advance after your confirmation.

---

## 1. Required tools (install once)

| Tool | Why we need it | Install link | Verify command |
|---|---|---|---|
| **Node.js LTS** (includes npm) | Run JavaScript outside the browser, install packages | https://nodejs.org/en/download/ (choose **LTS**) | `node -v` and `npm -v` |
| **Git** | Version control, push to GitHub | https://git-scm.com/download/win | `git --version` |
| **Visual Studio Code** | Code editor with integrated terminal, extensions | https://code.visualstudio.com/ | Open VS Code → `Help → About` shows version |
| **Web browser** (Chrome / Edge / Firefox) | View the pages you build | Any modern browser | Open `src/index.html` in the browser |
| **GitHub account** | Store your code online, collaborate | https://github.com/join | Sign in on github.com |

**How to verify everything works**
```powershell
node -v
npm -v
git --version
```
You should see version numbers (e.g., `v24.11.0`, `11.6.2`, `2.45.1.windows.1`).

---

## 2. Git configuration (one‑time)

```powershell
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```
Replace with your real name and the email you used for GitHub.

---

## 3. Project folder structure (already created)

```
C:\Users\hp\Documents\web-dev-journey\
├── README.md
├── state.json               # master progress tracker
├── progress.json            # quick lesson list
├── control.json             # wait / pass‑on state
├── references.json          # topic index for 'reference' queries
├── CONFIRMATION_PROTOCOL.md
├── SETUP_GUIDE.md           # this file
├── WAIT_PROTOCOL.md
├── REFERENCE_PROTOCOL.md
├── lessons/
│   ├── 01-setup.md
│   └── 02-html-css-landing.md
└── src/
    ├── index.html
    └── style.css
```

Open this folder in VS Code:
1. File → Open Folder → `C:\Users\hp\Documents\web-dev-journey`
2. Terminal → New Terminal (PowerShell)

---

## 4. How we communicate (the “commands”)

| Command | What it does | Advances lesson? |
|---|---|---|
| **`continue`** | Move to the next lesson (only after you confirm homework) | ✅ after `yes` |
| **`wait`** | Pause the current explanation | ❌ |
| **`pass on`** | Resume after a `wait` | ❌ |
| **`reference <chapter> <topic>`** | Simple explanation of a topic tied to the current lesson | ❌ |
| **any question** | Clarify something right now | ❌ |
| **`yes` / `no`** | Confirm / deny homework completion | ✅ on `yes` |

> **Rule:** I will **never** mark a lesson complete unless you explicitly reply **`yes`** to the confirmation question.

---

## 5. What you need from me

- Plain‑English, step‑by‑step explanations.
- All code shown in the lesson file (`lessons/XX-*.md`) and in `src/`.
- Real‑time verification of tools / commands.
- Immediate answers to `reference` queries.
- Respect for `wait` / `pass on` pauses.
- No advancement without your `yes`.

---

## 6. What I need from you

- Run the installers and verify commands.
- Complete the tiny homework at the end of each lesson.
- Tell me **`yes`** when you’ve truly finished it (or `no` if you need more help).
- Ask questions anytime — they never advance the lesson.
- Use `wait` / `pass on` if you need to step away.

---

## 7. Quick verification checklist (tick each)

- [ ] Node.js LTS installed → `node -v` shows version
- [ ] npm installed → `npm -v` shows version
- [ ] Git installed → `git --version` shows version
- [ ] Git global name & email set
- [ ] VS Code installed and can open the project folder
- [ ] Browser can open `src/index.html` (double‑click works)
- [ ] GitHub account created & you can sign in

When **all** items are ticked, reply **`yes`** and we’ll start Lesson 1 (Tools Setup) properly.

---

## 7.5 Recommended tech path (what companies hire for)

Stick with **full‑stack JavaScript** — one language everywhere:

| Lesson | What you learn | Used by |
|---|---|---|
| HTML + CSS | Page skeleton and styling | All frontend |
| JavaScript (ES6+) | Logic in the browser | All frontend |
| **TypeScript** | JavaScript with type safety | Pros / most jobs |
| **React** | Build dynamic UIs | Most hiring demand |
| **Node.js + Express** | Backend server (same language) | Backend |
| **PostgreSQL** | Main database (structured data) | Most apps |
| **Docker** | Package the app to run anywhere | Pros |
| **Expo** | Turn React into a mobile app | Mobile |

Why: one language (JS/TS), high demand, and you can ship a full web + mobile app without learning 5 different languages.

---

## 8. What happens after you say `yes`

1. I record the completion in `state.json` (add to `completedLessons`, set `homeworkDone: true`, increment `currentLesson` to 2).
2. I give you the Lesson 1 homework recap (just to confirm).
3. Then we move to **Lesson 2 — HTML + CSS landing page**.

---

**You’re ready when you’ve ticked everything above.**  
Just reply **`yes`** and we’ll begin.