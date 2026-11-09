# Mission 6: Git and GitHub

## 1. Task / Objective
Understand the basic Git workflow, create a branch, open a Pull Request, and build a Git command glossary.

## 2. Work Completed
- Explained core Git operations (status, add, commit, log) and the difference between staging and committing.
- Created branch `update-about`, added a "My Learning" section to the root README, committed, and pushed the branch.
- Opened a Pull Request from `update-about` → `main` on GitHub with description.
- Documented branch/PR purpose and created a 9-item Git command glossary.

## 3. Commands / Tools Used
| Command | Purpose |
| :--- | :--- |
| `git status` | Show working directory state (modified/staged/untracked files) |
| `git add <file>` | Stage specific file changes for commit |
| `git commit -m "msg"` | Create a commit snapshot with a message |
| `git log --oneline -5` | View recent commit history (compact) |
| `git checkout -b update-about` | Create and switch to new branch |
| `git push -u origin update-about` | Publish branch to GitHub remote |
| `git checkout main` / `git switch main` | Switch back to main branch |
| `git pull origin main` | Fetch and merge remote changes into local |

## 4. My Understanding

### Basic Git Workflow
- **Staging** (`git add`) prepares changes — it selects what goes into the next commit.
- **Committing** (`git commit`) creates a permanent, identified snapshot in history.
- You can stage multiple times before committing; only staged changes are recorded.

### Branch & Pull Request
- A **branch** is an independent development line. Work on `update-about` doesn't affect `main` until merged.
- A **Pull Request** proposes merging a branch into another. It shows diffs, enables review, and acts as a quality gate.
- **Collaboration value:** Parallel work without conflicts, code review before merge, traceable discussion on changes.

### Git Glossary
┌─────────────────────────┬─────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│      Git Operation      │                                          One-line Explanation                                           │
├─────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Initialise a repository │ git init creates a new .git directory, turning the current folder into a version-controlled repository. │
├─────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Check status            │ git status shows modified, staged, and untracked files compared to the last commit.                     │
├─────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Stage changes           │ git add <file> moves changes from working directory to the staging area for the next commit.            │
├─────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Commit changes          │ git commit -m "message" records a permanent snapshot of staged changes with a descriptive message.      │
├─────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ View history            │ git log (or git log --oneline) displays the chronological commit history with hashes and messages.      │
├─────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Create or list branches │ git branch <name> creates a branch; git branch lists all local branches.                                │
├─────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Switch branches         │ git checkout <branch> or git switch <branch> moves HEAD to the specified branch.                        │
├─────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Publish changes         │ git push -u origin <branch> uploads local commits to the remote repository on GitHub.                   │
├─────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Retrieve remote changes │ git pull fetches and merges changes from the remote branch into the current local branch.               │
└─────────────────────────┴─────────────────────────────────────────────────────────────────────────────────────────────────────────┘

---


## 5. Difficulties Faced
["No major issues."]

## 7. Evidence / Files
- Root `README.md` updated with "My Learning" section (visible in PR diff)
- Branch `update-about` pushed to GitHub
- Pull Request #1 created
- PR Status: **Merged**

## 8. Commit Details
| Commit Message | Branch | Pushed? |
| :--- | :--- | :--- |
| `Add My Learning section to root README` | `update-about` | ✅ Yes |
| `Document Git workflow, branch, PR, and glossary` | `main` (this commit) | ✅ Yes |
