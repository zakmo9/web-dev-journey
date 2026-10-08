# ⏸️ WAIT PROTOCOL — How to pause and resume me

Use this whenever you want to interrupt me mid-response, think through something, and then tell me to continue.

## The two keywords

| Keyword | What it does |
|---|---|
| **`wait`** | Tells me to **stop** right now. I save where I was and hold. |
| **`pass on`** | Tells me to **continue** from exactly where I stopped. I finish my response from the saved point. |

## How to use it

1. While I'm writing or loading, type **`wait`** and press Enter.
2. I will immediately stop, save my current position, and reply with a short "⏸️ Paused — waiting for you."
3. Go through the material at your own pace. Think, re-read, experiment.
4. When you're ready, type **`pass on`** and press Enter.
5. I will **resume from the exact point I was interrupted** and finish my response. Nothing is lost.

## What gets saved

Every time you say `wait`, I write to `control.json`:

```json
{
  "waitActive": true,
  "pausedAt": "2026-10-05T13:58:37Z",
  "pausedDuring": "Lesson 2 — writing the HTML/CSS landing page",
  "resumeKeyword": "pass on"
}
```

When you say `pass on`, I set `waitActive: false` and continue.

## Important rules

- **The lesson never moves during a wait.** `currentLesson` stays exactly where it was.
- **Your questions never advance the lesson.** Only an explicit "continue" or "next lesson" does.
- **The wait state is saved on disk**, so even if your computer restarts, the pause is recorded. Just reopen the folder and tell me "pass on" to resume.
- You can say `wait` multiple times — each pause is saved separately.
- If you forget whether you're paused, check `control.json` — if `waitActive` is `true`, you're paused.

## Quick resume after a reboot

1. Open `C:\Users\hp\Documents\web-dev-journey` in VS Code.
2. Look at `control.json` — if `waitActive` is `true`, you were paused.
3. Type **`pass on`** to resume from where you were interrupted.

## Example

```
You: "While you're explaining the CSS grid, wait."
Me: "⏸️ Paused — waiting for you. (saves control.json)"
... you think for 5 minutes ...
You: "pass on"
Me: "Continuing the CSS grid explanation from where I stopped: ..."
```