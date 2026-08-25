# Git & GitHub Cheat Sheet

A quick reference for common Git commands and workflows.

---

## 1. Setup & Configuration

```bash
git config --global user.name "Your Name"
```

Set global username.

```bash
git config --global user.email "you@example.com"
```

Set global email.

```bash
git config --global core.editor code
```

Set default editor.

```bash
git config --list
```

List all configuration.

```bash
git config --global --list
```

List global configuration.

```bash
git config --local --list
```

List local configuration.

---

## 2. Start a Project

```bash
git init
```

Initialize a new Git repository.

```bash
git clone <repo-url>
```

Clone/download a repository.

```bash
git clone <repo-url> <dir>
```

Clone a repository into a specific directory.

---

## 3. Daily Workflow

```bash
git status
```

Show working tree status.

```bash
git add <file>
```

Stage a specific file.

```bash
git add .
```

Stage all changes.

```bash
git commit -m "message"
```

Commit staged changes.

```bash
git commit -am "message"
```

Stage tracked changes and commit them.

```bash
git log
```

Show commit history.

```bash
git log --oneline --graph --all
```

Show a compact commit history graph.

```bash
git diff
```

Show unstaged changes.

```bash
git diff --staged
```

Show staged changes.

```bash
git show <commit>
```

Show details of a commit.

---

## 4. Branching & Merging

```bash
git branch
```

List branches.

```bash
git branch -a
```

List all branches.

```bash
git branch <branch-name>
```

Create a new branch.

```bash
git checkout <branch-name>
```

Switch to a branch.

```bash
git checkout -b <branch-name>
```

Create and switch to a new branch.

```bash
git merge <branch-name>
```

Merge a branch into the current branch.

```bash
git branch -d <branch>
```

Delete a branch safely.

```bash
git branch -D <branch>
```

Force-delete a branch.

---

## 5. Remotes

```bash
git remote -v
```

List remotes.

```bash
git remote add origin <url>
```

Add a new remote.

```bash
git remote remove <name>
```

Remove a remote.

```bash
git fetch <remote>
```

Fetch changes without merging.

```bash
git pull
```

Fetch and merge changes.

```bash
git pull --rebase
```

Fetch and rebase local commits.

```bash
git push <remote> <branch>
```

Push a branch to a remote repository.

```bash
git push -u origin <branch>
```

Push a branch and set its upstream.

```bash
git push --tags
```

Push all tags.

> **Warning:** `git push --force` can overwrite remote history. Use it with caution.

---

## 6. Stash

```bash
git stash
```

Stash local changes.

```bash
git stash push -m "message"
```

Stash changes with a message.

```bash
git stash list
```

List all stashes.

```bash
git stash show
```

Show stash changes.

```bash
git stash pop
```

Apply and remove the latest stash.

```bash
git stash apply
```

Apply the latest stash while keeping it in the stash list.

```bash
git stash drop
```

Remove the latest stash.

```bash
git stash clear
```

Remove all stashes.

---

## 7. Undo & Revert

```bash
git checkout -- <file>
```

Discard changes in a file.

```bash
git reset <file>
```

Unstage a file.

```bash
git reset --soft <commit>
```

Move `HEAD` while keeping changes staged.

```bash
git reset --mixed <commit>
```

Move `HEAD` while unstaging changes.

```bash
git reset --hard <commit>
```

Move `HEAD` and discard changes.

> **Warning:** `git reset --hard` can permanently discard uncommitted changes.

```bash
git revert <commit>
```

Revert a commit safely by creating a new commit.

```bash
git revert HEAD
```

Revert the latest commit.

```bash
git commit --amend
```

Amend the last commit.

```bash
git rebase <branch>
```

Rebase the current branch onto another branch.

```bash
git rebase -i HEAD~n
```

Interactively rebase the last `n` commits.

---

## 8. Tagging

```bash
git tag
```

List tags.

```bash
git tag <tagname>
```

Create a lightweight tag.

```bash
git tag -a <tagname> -m "msg"
```

Create an annotated tag.

```bash
git show <tagname>
```

Show tag details.

```bash
git push origin <tagname>
```

Push a tag to the remote.

```bash
git push origin --tags
```

Push all tags.

---

## 9. Submodules

```bash
git submodule add <url> <path>
```

Add a submodule.

```bash
git submodule init
```

Initialize submodules.

```bash
git submodule update
```

Update submodules.

```bash
git submodule update --init --recursive
```

Initialize and update submodules recursively.

```bash
git submodule foreach git pull origin main
```

Pull changes in all submodules.

---

## Common Workflow

```text
Working Directory
       │
       ▼
   git add
       │
       ▼
Staging Area
       │
       ▼
  git commit
       │
       ▼
Repository
       │
       ▼
   git push
       │
       ▼
Remote Repository
```

### Typical Git Flow

```bash
git status
git add .
git commit -m "your message"
git pull --rebase
git push
```

---

## Other Useful Commands

```bash
git help <command>
```

Get help for a command.

```bash
git --version
```

Show the installed Git version.

```bash
git config --list
```

Show Git configuration.

```bash
git remote -v
```

List configured remotes.

```bash
git log --graph --oneline --all
```

View a compact commit history graph.

---

## Quick Reference

| Task                   | Command                   |
| ---------------------- | ------------------------- |
| Initialize repo        | `git init`                |
| Clone repo             | `git clone <repo-url>`    |
| Check status           | `git status`              |
| Stage file             | `git add <file>`          |
| Stage everything       | `git add .`               |
| Commit                 | `git commit -m "message"` |
| View history           | `git log`                 |
| Create branch          | `git branch <name>`       |
| Switch branch          | `git checkout <name>`     |
| Create + switch branch | `git checkout -b <name>`  |
| Merge branch           | `git merge <name>`        |
| Pull changes           | `git pull`                |
| Push changes           | `git push`                |
| Stash changes          | `git stash`               |
| Undo commit safely     | `git revert <commit>`     |
| Create tag             | `git tag <name>`          |
| View remotes           | `git remote -v`           |

---



