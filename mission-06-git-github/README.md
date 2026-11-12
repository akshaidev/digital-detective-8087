# Mission 6 - Git and GitHub

## 1. Task / objective
Practice the core Git workflow, create a feature branch (`update-about`), update the root `README.md`, publish the branch to GitHub to open a Pull Request, merge changes, and build a Git command glossary.

## 2. Work completed
* Inspected repository status and recent commit history (`git status`, `git log`).
* Created the `update-about` branch, added a `"My Learning"` section to `README.md`, and committed the update.
* Pull Request status: Created via `gh pr create` (https://github.com/akshaidev/digital-detective-8087/pull/1), merged locally into `main`, and pushed to GitHub.
* Documented the nine core Git commands in a one-line glossary.

## 3. Commands / tools used
* `git status`, `git add`, `git commit`, `git log` — Core local commit workflow commands.
* `git checkout -b update-about` & `git checkout main` — Branch creation and switching commands.
* `git push -u origin update-about`, `gh pr create`, `git merge`, `git push origin main` — Published branch, opened PR, merged locally, and pushed `main`.

## 4. My understanding
### Task 6.1 — Basic Git Workflow
* **Staging vs. Committing:** Staging (`git add`) places specific modified files into the **index/staging area** so you can review and group exactly what belongs in the next snapshot. Committing (`git commit`) permanently records that staged snapshot into the repository's history with a descriptive message.
* **Observed `git log -n 5 --oneline`:**

```text
c6581ab Build number converter and practise data representation
45cc091 Compare compilers and interpreters
0d59cff Document operating system and file management
34a877b Complete Terminal and file management mission
ac31473 Complete computer basics and IPOS mission
```

| Git operation | What it does in your own words |
| :--- | :--- |
| **Check repository status** (`git status`) | Shows the current branch along with modified, staged, and untracked files. |
| **Stage selected changes** (`git add`) | Adds chosen file changes to the staging area in preparation for a commit. |
| **Create a commit** (`git commit`) | Saves a permanent snapshot of staged changes to the local Git history. |
| **View commit history** (`git log`) | Displays past commits chronologically with commit hashes, authors, dates, and messages. |

### Task 6.3 — Branches and Pull Requests
* **Branch & Pull Request Purpose:** A **branch** is an independent line of development that lets you build features or edit docs without destabilizing `main`. A **Pull Request (PR)** on GitHub proposes merging changes from one branch into another, giving teammates or instructors a clean diff view to review, comment on, and approve code before merging.
* **Pull Request Status:** Created via `gh pr create` (https://github.com/akshaidev/digital-detective-8087/pull/1), merged locally into `main`, and pushed to GitHub.

### Task 6.4 — Git Command Glossary
* **Initialise a repository (`git init`):** Creates a new `.git` directory to start tracking a project with Git.
* **Check status (`git status`):** Lists which files are modified, staged, or untracked on the current branch.
* **Stage changes (`git add <file>`):** Moves file modifications into the staging area for the next commit.
* **Commit changes (`git commit -m "msg"`):** Records staged changes as a permanent commit in version history.
* **View history (`git log`):** Shows the sequence of previous commits and their metadata.
* **Create or list branches (`git branch`):** Lists existing local branches or creates a new branch pointer.
* **Switch branches (`git checkout <branch>` / `git switch <branch>`):** Updates the working directory to match a target branch.
* **Publish changes (`git push`):** Uploads local commits and branches to a remote repository such as GitHub.
* **Retrieve remote changes (`git pull`):** Fetches new commits from a remote repository and merges them into the current branch.

## 5. Difficulties faced
No major difficulties.

## 6. How I resolved them
Not applicable.

## 7. Evidence / files
* `mission-06-git-github/README.md`
* `evidence/safe-outputs.txt`
* Branch `update-about` and Pull Request status: Created via `gh pr create` (https://github.com/akshaidev/digital-detective-8087/pull/1), merged locally into `main`, and pushed to GitHub.

## 8. Commit details
* **Commit message:** `Complete Git and GitHub collaboration mission`
* **Status:** Committed and pushed to GitHub on `main`.
