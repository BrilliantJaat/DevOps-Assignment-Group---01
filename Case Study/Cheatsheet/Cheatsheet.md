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

# GIT + GITLAB CHEATSHEET

## 1. GIT SETUP

```bash
git --version

git config --global user.name "Your Name"

git config --global user.email "you@example.com"

git config --list
```

---

## 2. CREATE / CLONE REPOSITORY

```bash
# Create new repository
git init

# Clone GitLab repository
git clone https://gitlab.com/username/project.git

# Clone into specific folder
git clone https://gitlab.com/username/project.git my-project
```

---

## 3. CHECK STATUS

```bash
git status
```

---

## 4. ADD AND COMMIT

```bash
# Add one file
git add filename.txt

# Add all files
git add .

# Commit changes
git commit -m "Your commit message"

# Add and commit tracked files
git commit -am "Your commit message"
```

---

## 5. BRANCHES

```bash
# List branches
git branch

# Create branch
git branch feature-login

# Switch branch
git switch feature-login

# Create and switch to branch
git switch -c feature-login

# Delete branch
git branch -d feature-login

# Force delete branch
git branch -D feature-login
```

---

## 6. PUSH / PULL

```bash
# Push changes
git push

# Push new branch
git push -u origin feature-login

# Pull latest changes
git pull

# Download changes without merging
git fetch

# Fetch all branches
git fetch --all
```

---

## 7. REMOTE REPOSITORY

```bash
# Show remote repositories
git remote -v

# Add GitLab remote
git remote add origin https://gitlab.com/username/project.git

# Change remote URL
git remote set-url origin https://gitlab.com/username/project.git

# Remove remote
git remote remove origin
```

---

## 8. GIT LOG / HISTORY

```bash
# Full commit history
git log

# Short commit history
git log --oneline

# Graph view
git log --oneline --graph --all

# Show specific commit
git show <commit-id>

# Show last 5 commits
git log -5
```

---

## 9. CHECK CHANGES

```bash
# Show unstaged changes
git diff

# Show staged changes
git diff --staged

# Compare two commits
git diff <commit1> <commit2>
```

---

## 10. UNDO CHANGES

```bash
# Undo changes in a file
git restore filename.txt

# Undo all unstaged changes
git restore .

# Unstage a file
git restore --staged filename.txt

# Undo last commit but keep changes staged
git reset --soft HEAD~1

# Undo last commit and unstage changes
git reset --mixed HEAD~1

# Undo last commit and DELETE changes
git reset --hard HEAD~1

# Safely undo a commit
git revert <commit-id>

# Change last commit message
git commit --amend -m "New commit message"
```

---

## 11. STASH

```bash
# Save current changes
git stash

# Save with message
git stash push -m "My changes"

# List stashes
git stash list

# Apply latest stash
git stash apply

# Apply and remove latest stash
git stash pop

# Delete stash
git stash drop
```

---

## 12. MERGE

```bash
# Switch to main
git switch main

# Get latest main
git pull

# Merge feature branch
git merge feature-login

# Push merged changes
git push
```

---

## 13. MERGE CONFLICT

```bash
# Check conflicts
git status

# After fixing conflicts
git add .

git commit -m "Resolve merge conflict"

git push
```

---

## 14. REBASE

```bash
# Switch to feature branch
git switch feature-login

# Rebase with main
git rebase main

# After resolving conflict
git add .

git rebase --continue

# Cancel rebase
git rebase --abort
```

---

# GITLAB WORKFLOW

```bash
# 1. Clone repository
git clone https://gitlab.com/username/project.git

# 2. Enter project
cd project

# 3. Switch to main
git switch main

# 4. Get latest changes
git pull

# 5. Create feature branch
git switch -c feature/login

# 6. Make your changes

# 7. Check changes
git status

# 8. Add changes
git add .

# 9. Commit
git commit -m "Add login feature"

# 10. Push branch to GitLab
git push -u origin feature/login
```

Then:

```text
GitLab
   ↓
Create Merge Request
   ↓
Code Review
   ↓
CI/CD Pipeline
   ↓
Approval
   ↓
Merge into main
```

---

# GITLAB CI/CD

File:

```text
.gitlab-ci.yml
```

Basic example:

```yaml
stages:
  - build
  - test
  - deploy

build:
  stage: build
  script:
    - echo "Building application"

test:
  stage: test
  script:
    - echo "Running tests"

deploy:
  stage: deploy
  script:
    - echo "Deploying application"
```

---

# GITLAB CI VARIABLES

```yaml
my_job:
  script:
    - echo "$MY_VARIABLE"
```

Store secrets in:

```text
GitLab
→ Settings
→ CI/CD
→ Variables
```

DO NOT put passwords, API keys, or private keys directly in `.gitlab-ci.yml`.

---

# GITLAB ARTIFACTS

```yaml
build:
  script:
    - npm run build

  artifacts:
    paths:
      - dist/
```

---

# IMPORTANT GIT COMMANDS

```bash
git init
git clone <url>

git status

git add .
git commit -m "message"

git push
git pull
git fetch

git branch
git switch -c <branch>
git switch <branch>

git merge <branch>
git rebase <branch>

git log --oneline
git diff

git stash
git stash pop

git restore <file>
git revert <commit>
```

---

# MOST COMMON DAILY WORKFLOW

```bash
git switch main
git pull

git switch -c feature/my-feature

# Make changes

git status
git add .
git commit -m "Add my feature"

git push -u origin feature/my-feature
```

Then create a **Merge Request in GitLab** and merge the branch after review.



    



  





  



  



