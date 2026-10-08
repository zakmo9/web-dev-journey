# Lesson 1 — Setting Up Your Computer (Like Building Your Toolbox)

> **Why this exists as a file:** Your computer might turn off. So we *write* every lesson here on disk. Open `progress.json` whenever you want to see where you stopped, and I'll keep writing lessons in this `lessons` folder so you never lose your spot.

## Learning goals (the kid version)
Think of building a website like building with LEGO + drawing + telling a story.
Before we build anything, we need the right tools on our computer. This lesson is just collecting the tools.

Tools we will install today:
1. **Node.js** — gives us a mini computer program runner so our website can *do* things (like save data). Comes with **npm** (a robot that fetches extra LEGO pieces).
2. **Visual Studio Code (VS Code)** — the notebook where we write all our code.
3. **Git** — a magic "undo button" that remembers every version of our work.
4. A **GitHub** account — like Google Drive, but for code (and it helps us show our work to others).

---

## Step 1.1 — Install Node.js (this also gives us npm)

Go to: <https://nodejs.org>
- Click the big **green button** that says *LTS* (Long Term Support = stable, boring = good).
- Run the file it downloads. Click "Next" a few times, leave all checkboxes checked.
- When it finishes, let's check it worked.

> How to "check": open the **Terminal**
> - Press `Win + R`, type `cmd`, press Enter. A black window called **Command Prompt** opens.
> - Type exactly:
> ```
> node -v
> npm -v
> ```
> - You should see two numbers, like `v20.18.0` and `10.5.0`. That means Node and npm are installed!

---

## Step 1.2 — Install VS Code (your code notebook)

Go to: <https://code.visualstudio.com>
- Click **Download** (it picks Windows for you automatically).
- Run it and click "Next" until it finishes.
- Open VS Code.
- In VS Code, press `Ctrl + Shift + P` (that's Control + Shift + the letter P). Type `shell`. Choose **"Command Prompt"** or **"Git Bash"** as your terminal (we'll pick Git Bash in a minute — for now Command Prompt is fine).

---

## Step 1.3 — Install Git (the undo button)

Go to: <https://git-scm.com>
- Click **Download** (it gives you the Windows file).
- Run it. Click "Next" for everything, but when it asks about the **"default editor"** choose **Nano** is fine, or just leave the default.
- When it asks **"Choosing the SSH executable"** or anything about SSH, just click "Next".
- Important: when it asks **"How should Git handle line endings?"** choose **"Git from Git Bash Only"** (or just click Next).
- Click "Install".

Check it worked:
```
git --version
```
You should see something like `git version 2.49.0.windows.1`.

---

## Step 1.4 — Make a GitHub account

Go to: <https://github.com>
- Click **Sign up**.
- Use your real email (GitHub will email you to confirm).
- Pick a password you'll remember.
- Done. (We will connect this to our computer in Lesson 3.)

---

## Step 1.5 — Verify everything (the grown-up version)

Open VS Code. In VS Code, open the **Terminal**:
- Top menu → **Terminal** → **New Terminal** (or press `` Ctrl + ` ``).
- In the terminal that opens, type:
```
node -v
npm -v
git --version
```
All three should print version numbers. ✅ If any says "'command not found'", re-open VS Code (it needs to be reopened to see new tools).

---

## What is a "Terminal"? (explained simply)

A **terminal** is a text box where you tell the computer to do things by typing commands, like:
- "make a new folder"
- "install this plugin"
- "run my website"

We will use it a LOT. Don't be scared. Every command I give you, you can copy + paste with `Ctrl + V`.

---

## Quick glossary (words you’ll hear a lot)
| Word | Simple meaning |
|---|---|
| **Package** | A ready-made piece of code someone else wrote (fetched by npm) |
| **Repository / repo** | A folder that holds all our project files (we'll put it on GitHub) |
| **Terminal** | Text box for giving the computer commands |
| **Port** | A number that says "this website lives here" (like an apartment number) |
| **Server** | A computer (or program) that sends and receives data |

---

## Your homework (5 minutes, very easy)
1. Install Node.js, VS Code, and Git using the links above.
2. In a fresh terminal, run:
```
node -v
npm -v
git --version
```
3. Take a screenshot of the three version numbers and **save it on your computer** (this proves your tools work).

> Next lesson: we draw our first webpage with **HTML** (the structure) and **CSS** (the colors and layout), and build a real **landing page**.

---

**Progress tracker:** see `state.json` in the project root — it records exactly what I last did and where to resume.

---

## 🧭 Checkpoint — Where we left off
- **Saved:** `state.json` at `2026-10-05T12:03:15Z` — "Wrote progress.json, README.md, lessons/01-setup.md. Project workspace created."
- **Current:** Lesson 1 is done. **Homework:** install Node.js, VS Code, Git; run `node -v`, `npm -v`, `git --version`; screenshot the results.
- **Next lesson:** HTML + CSS landing page.
- **To resume:** tell me "continue" or edit `state.json` → `currentLesson`.
