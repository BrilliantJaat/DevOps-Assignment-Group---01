# GIT

## 1. Introduction to Git

**Git** is a **distributed version control system (DVCS)** used to track and manage changes in source code and other files.

It helps developers to:

* Track changes in files and code
* Maintain different versions of a project
* Work on projects with multiple developers
* Restore previous versions when required
* Work on different features using branches

Git was created by **Linus Torvalds** in 2005.

---

## 2. Features of Git

The main features of Git are:

* **Distributed:** Every developer has a complete copy of the repository.
* **Fast:** Most Git operations are performed locally.
* **Version Control:** It keeps track of changes made to files.
* **Branching:** Developers can create separate branches for different features.
* **Merging:** Changes from different branches can be combined.
* **Secure:** Git uses hashing to maintain the integrity of data.
* **Collaboration:** Multiple developers can work on the same project.

---

## 3. Git Repository

A **Git repository** is a storage location where Git tracks all the files, changes, commits, and history of a project.

A repository can be:

* **Local Repository:** Stored on the developer's computer.
* **Remote Repository:** Stored on a remote platform such as GitHub or GitLab.

---

## 4. Git Working Areas

Git mainly works with three areas:

### 4.1 Working Directory

The **Working Directory** contains the actual project files where developers make changes.

### 4.2 Staging Area

The **Staging Area** contains the changes that are selected to be included in the next commit.

The `git add` command is used to move changes from the Working Directory to the Staging Area.

### 4.3 Local Repository

The **Local Repository** stores committed changes and the complete project history.

The `git commit` command saves the staged changes into the local repository.

### Git Workflow

```text
Working Directory
       ↓
   git add
       ↓
Staging Area
       ↓
  git commit
       ↓
Local Repository
       ↓
   git push
       ↓
Remote Repository
```

---

## 5. Important Git Commands

### 5.1 git --version

Used to check whether Git is installed and to display its version.

```bash
git --version
```

### 5.2 git config

Used to configure the username and email used for Git commits.

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

### 5.3 git init

Creates a new Git repository in the current directory.

```bash
git init
```

### 5.4 git clone

Creates a local copy of an existing remote repository.

```bash
git clone <repository-url>
```

### 5.5 git status

Shows the current status of files in the repository.

```bash
git status
```

### 5.6 git add

Moves changes from the Working Directory to the Staging Area.

```bash
git add filename
```

To add all changed files:

```bash
git add .
```

### 5.7 git commit

Saves staged changes to the local repository with a message.

```bash
git commit -m "Add new changes"
```

### 5.8 git log

Displays the history of commits.

```bash
git log
```

### 5.9 git diff

Shows the differences between file versions or changes that have not been staged.

```bash
git diff
```

### 5.10 git branch

Used to create, view, or manage branches.

```bash
git branch
```

To create a new branch:

```bash
git branch feature
```

### 5.11 git switch

Used to switch from one branch to another.

```bash
git switch feature
```

A new branch can also be created and switched to using:

```bash
git switch -c feature
```

### 5.12 git merge

Combines changes from one branch into another branch.

```bash
git merge feature
```

### 5.13 git pull

Downloads the latest changes from a remote repository and integrates them into the current branch.

```bash
git pull
```

### 5.14 git push

Uploads local commits to a remote repository.

```bash
git push
```

---

## 6. Git Branching

A **branch** is a separate line of development in a Git repository.

Branches allow developers to work on different features without directly affecting the main code.

For example:

```text
main
 |
 |------ feature-login
 |
 |------ feature-payment
 |
 |------ bug-fix
```

After completing and testing a feature, its branch can be merged into the main branch.

### Advantages of Branching

* Allows parallel development
* Keeps new features separate
* Makes testing safer
* Helps developers work independently
* Makes collaboration easier

---

## 7. Git Merge

**Git Merge** is used to combine changes from one branch into another branch.

For example, if a developer creates a `feature` branch from `main`, completes the feature, and wants to add it to `main`, the feature branch can be merged into `main`.

```bash
git switch main
git merge feature
```

---

## 8. Git vs Traditional Version Control

Traditional version control systems may depend heavily on a central server.

Git is a **distributed version control system**, so every developer normally has a complete local repository.

### Benefits of Git

* Works offline for many operations
* Fast performance
* Complete project history locally
* Easy branching and merging
* Supports distributed development

---

## 9. Advantages of Git

* Free and open-source
* Fast and lightweight
* Distributed architecture
* Powerful branching and merging
* Tracks complete project history
* Supports teamwork and collaboration
* Can work without an internet connection for many operations
* Helps recover previous versions of files

---

## 10. Git and Remote Repositories

Git manages version control locally, while remote repositories provide a place to store and collaborate on Git repositories online.

Popular platforms that host Git repositories include:

* GitHub
* GitLab
* Bitbucket

Git itself is different from these platforms.

**Git = Version Control System**

**GitHub/GitLab = Platforms for hosting and collaborating on Git repositories**

---

## 11. Basic Git Workflow

A basic Git workflow is:

```bash
git clone <repository-url>
git status
git add .
git commit -m "Make changes"
git pull
git push
```

The general process is:

```text
Create/Clone Repository
        ↓
Make Changes
        ↓
Check Status
        ↓
Stage Changes
        ↓
Commit Changes
        ↓
Pull Latest Changes
        ↓
Push Changes
```

---

## 12. Conclusion

Git is an important **distributed version control system** used to manage and track changes in software projects. It provides features such as **version control, branching, merging, collaboration, and project history**. Git is widely used in software development and works with remote repository platforms such as **GitHub and GitLab**.

