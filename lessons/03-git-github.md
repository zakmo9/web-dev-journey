# Lesson 3 — Git + GitHub: Saving Versions & Showing Your Work Online

## The story (for a 10-year-old)

Imagine you're drawing a comic book. Every time you finish a page, you want to save it so you can:
- Go back to an earlier version if you mess up
- Show your friends the latest page
- Work on different chapters without losing your work

**Git** is your comic book backup system. **GitHub** is the website where you show your comic to the world.

---

## What is Git?

Git = a **version control system**. It tracks every change you make to your files over time.

- Every time you save work, Git records: **what changed, when, and by whom**
- You can go back to any previous version
- You can experiment safely — if you break something, just revert

## What is GitHub?

GitHub = a website that hosts Git repositories (online hard drives for your code).

- Your code lives at `github.com/your-username/repo-name`
- Other people can see it, clone it, or contribute to it
- It's your **portfolio** — proof you know how to code

---

## The Git workflow (basic)

```bash
git init              # Start a new Git repo in this folder
git add .             # Tell Git "track these files"
git commit -m "message"  # Save a snapshot of your work
git remote add origin <URL>  # Connect to GitHub
git push -u origin main    # Upload your code to GitHub
```

---

## Step-by-step setup

### Step 1: Configure your Git identity

Before you commit, tell Git who you are:

```bash
git config --global user.name "zakmo9"
git config --global user.email "your-email@example.com"
```

Replace the email with the one you used for GitHub.

### Step 2: Initialize a Git repo

```bash
git init
```

This creates a hidden `.git` folder that tracks all your changes.

### Step 3: Create a `.gitignore` file

Some files shouldn't be tracked (like node_modules, .env files). Create a `.gitignore`:

```bash
# .gitignore
node_modules/
.env
.DS_Store
```

### Step 4: Add and commit your files

```bash
git add .
git commit -m "Initial commit: Islam Home landing page (HTML + CSS)"
```

### Step 5: Create a GitHub repository

1. Go to [github.com](https://github.com)
2. Click **New** (green button)
3. Name it: `web-dev-journey`
4. Make it **Public** (so others can see your work)
5. Click **Create repository**

### Step 6: Connect to GitHub

Copy the repository URL (it looks like `https://github.com/zakmo9/web-dev-journey.git`), then:

```bash
git remote add origin https://github.com/zakmo9/web-dev-journey.git
```

### Step 7: Push your code

```bash
git push -u origin main
```

If Git asks for a username/password:
- **Username:** your GitHub username (`zakmo9`)
- **Password:** your GitHub password **OR** a Personal Access Token (PAT)

---

## What you'll see after pushing

Your code is now online at `github.com/zakmo9/web-dev-journey`. Anyone can view it.

---

## Key Git commands to remember

| Command | What it does |
|---|---|
| `git status` | See what files changed, what's staged, what's not |
| `git add .` | Stage all changes for the next commit |
| `git commit -m "msg"` | Save a snapshot of staged changes |
| `git log` | See the history of all commits |
| `git diff` | See exactly what changed in a file |
| `git push` | Upload your commits to GitHub |
| `git pull` | Download changes from GitHub |
| `git clone <URL>` | Copy a repo from GitHub to your computer |

---

## Homework (20 min)

1. Complete Steps 1-7 above.
2. Verify your code is online: visit `github.com/zakmo9/web-dev-journey`
3. Take a screenshot of your repo page.

> Next lesson: JavaScript fundamentals — the brain of your web pages.

---

## 🧭 Checkpoint — Where we left off
- **Saved:** `state.json` at `2026-10-08T22:05:28Z` — "Lesson 2 completed. Advancing to Lesson 3."
- **Current:** Lesson 3 — Git + GitHub.
- **Current files:** `web-dev-journey/` folder with `src/index.html`, `src/style.css`, `lessons/`, etc.
- **Next lesson:** JavaScript fundamentals.
- **To resume:** tell me "continue" or edit `state.json` → `currentLesson`.