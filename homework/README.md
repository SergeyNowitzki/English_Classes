# Homework

Pupils receive tasks and send finished work in this repository.

- `main` contains lessons, assignments, and approved work.
- Each pupil has a separate branch: `pupil/<name>`, for example
  `pupil/anna-k`.
- A pull request is the place where the teacher checks the answer, adds inline
  comments, and requests corrections.

```
homework/
  assignments/                 ← tasks published by the teacher on main
    2026-09-26-fire-writing/
      task.md
  pupils/                      ← answers submitted from individual branches
    anna-k/
      2026-09-26-fire-writing/
        answer.md
    ivan-p/
      2026-09-26-fire-writing/
        answer.md
```

Use the same task folder name in `assignments/` and in the pupil’s folder, so the teacher can match them.

## Teacher — publish a task (main)

1. On `main`, add `homework/assignments/<date-topic>/task.md` (or an `.html` page).
2. Commit and push `main`.
3. Tell the class the folder name, for example `2026-09-26-fire-writing`.

## Teacher — create one branch per pupil

Do this once for each pupil:

```bash
git checkout main
git pull
git checkout -b pupil/anna-k
git push -u origin pupil/anna-k
git checkout main
```

Replace `anna-k` with the pupil's short lowercase name. Give the pupil write
access to the GitHub repository so they can push to their branch.

## Pupil — first setup

```bash
git clone git@github.com:SergeyNowitzki/English_Classes.git
cd English_Classes
git checkout pupil/anna-k
```

Replace `anna-k` with your assigned branch name.

## Pupil — receive a new task

Update your branch with the newest assignments from `main`:

```bash
git checkout pupil/anna-k
git fetch origin
git merge origin/main
```

The new task is under `homework/assignments/<task-name>/`.

## Pupil — send the finished task

Write only in your folder, for example
`homework/pupils/anna-k/<task-name>/answer.md`.

```bash
git checkout pupil/anna-k
git pull
# create or edit homework/pupils/anna-k/<task-name>/answer.md
git add homework/pupils/anna-k/
git commit -m "Homework: <task-name>"
git push
```

On GitHub, open a pull request:

- **base:** `main`
- **compare:** `pupil/anna-k`
- title: `Homework: <task-name> — Anna`

## Teacher — verify and comment

1. Open the pupil's pull request on GitHub.
2. Use **Files changed** to comment on an exact sentence or line.
3. Choose **Request changes** if the pupil must correct something.
4. The pupil edits the answer and pushes again; the same pull request updates
   automatically.
5. When the work is ready, choose **Approve** and **Merge pull request**. Use
   **Create a merge commit** for these long-lived branches, rather than
   **Squash and merge**.
6. For the next assignment, the pupil merges the updated `main` into their
   same branch again.

Do not delete the pupil's branch after merging; it is reused for later homework.

> **Privacy:** branches are not private folders. Everyone who can access this
> repository can normally see every branch and every pupil's work. Use separate
> private repositories if answers must be confidential.
