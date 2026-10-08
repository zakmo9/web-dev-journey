# CONFIRMATION PROTOCOL

This protocol guarantees that a lesson is **only marked complete after the user confirms they have done the work**.

## When to use
- At the end of **every** lesson (1, 2, 3, … 11).
- Never mark a lesson complete just because the lesson file was written.

## Flow
1. The assistant finishes teaching a lesson and gives the homework.
2. The assistant **asks the user directly**: "Have you completed the homework for Lesson N? Reply 'yes' or 'no'."
3. The user replies **yes** → the assistant records the completion in `state.json` and advances `currentLesson` to N+1.
4. The user replies **no** (or anything else) → the lesson stays at N and the assistant re‑explains the homework.

## State fields updated on "yes"
- `completedLessons` gets the lesson number appended.
- `inProgress.homeworkDone` set to `true`.
- `inProgress.lastAction` records the confirmation.
- A checkpoint entry is added.
- `currentLesson` is incremented by 1.
- `currentLessonTitle` is updated to the next lesson title.

## Lesson titles
| Lesson | Title |
|---|---|
| 1 | Tools Setup |
| 2 | HTML + CSS landing page |
| 3 | Git & GitHub |
| 4 | JavaScript frontend |
| 5 | Node.js & Express backend |
| 6 | MongoDB |
| 7 | Project folder structure |
| 8 | REST APIs |
| 9 | Socket.IO real-time |
| 10 | Expo mobile app |
| 11 | Responsive design & deployment |

## Do NOT advance on
- Questions asked during the lesson
- `reference` queries
- `wait` / `pass on` commands