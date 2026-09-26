# English Classes

Materials for English lessons: complete classes, grammar, vocabulary, skills practice, and tests.

This repository is organised for a teacher, not for a software project. Open a folder, read its `README.md`, and drop new files next to similar ones.

## How to find something

| I need… | Go to |
|---|---|
| A ready-to-teach class | [`lessons/`](lessons/README.md) |
| Rules, tables, drills for one grammar point | [`grammar/`](grammar/README.md) |
| Topic word lists and collocations | [`vocabulary/`](vocabulary/README.md) |
| Extra reading / writing / speaking / listening | [`skills/`](skills/README.md) |
| Quizzes and tests | [`assessments/`](assessments/README.md) |
| Homework: give a task or collect pupil work | [`homework/`](homework/README.md) |
| A blank lesson to copy | [`templates/`](templates/README.md) |

Levels follow CEFR: **A1, A2, B1, B1+, B2, C1**. Put the level in the lesson folder name or at the top of the file.

## Open an HTML lesson in the browser

Git and GitHub store HTML as **source code**. That is normal. The pretty page appears when a browser opens the file.

On this Mac:

1. In Finder, go to the lesson folder and **double-click** `lesson.html`.
2. Or in Terminal: `open path/to/lesson.html`.
3. In Cursor / VS Code, right-click the file → **Reveal in Finder**, then double-click. Clicking the file in the editor shows the code so you can edit it.

To share a clickable website from GitHub later, GitHub Pages can publish the `lessons/` HTML. Until then, send the `.html` file or open it locally.

## One homework branch per pupil

Teacher materials and assignments stay on `main`. Every pupil has a separate
long-lived branch, such as **`pupil/anna-k`** or **`pupil/ivan-p`**.

1. The teacher publishes a task under `homework/assignments/` on `main`.
2. The pupil updates their branch from `main`, completes the task, and pushes
   the answer to their own branch.
3. The pupil opens a pull request to `main`.
4. The teacher comments on the work, requests corrections if needed, and
   approves and merges the final version.

Full steps for the teacher and for pupils are in [`homework/README.md`](homework/README.md).

## Naming

- Folders: lowercase, hyphens (`fire-retire-at-40`)
- One folder per complete lesson
- Keep teacher notes in that same folder (`teacher-notes.md`) if they should not appear on the student page
