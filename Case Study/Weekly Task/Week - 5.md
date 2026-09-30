# Week 5 - Git Collaboration & Team Workflow

## Objective

To understand how developers collaborate on a shared project using Git and GitHub, and learn the basic team workflow.

## Introduction

Git collaboration allows multiple developers to work on the same project. Developers can create branches, make changes, commit updates, and merge their work into the main branch.

## Important Concepts

* **Clone:** Download a remote repository to a local computer.
* **Remote:** A reference to a repository hosted online.
* **Push:** Upload local commits to a remote repository.
* **Pull:** Download and integrate remote changes.
* **Pull Request:** A request to review and merge proposed changes.
* **Merge Conflict:** A situation where Git cannot automatically combine certain changes.

## Important Git Commands

```bash
git clone <repository-url>
git remote -v
git pull origin main
git switch -c feature
git add .
git commit -m "Added new feature"
git push -u origin feature
```

## Team Collaboration Workflow

1. Clone the shared repository.
2. Create a separate branch for your task.
3. Make changes to project files.
4. Stage and commit the changes.
5. Push the branch to GitHub.
6. Create a Pull Request.
7. Review the changes and merge the branch.

## Practical Work

1. Opened a GitHub repository.
2. Cloned the repository or opened an existing local project.
3. Created a new feature branch.
4. Made a change to a project file.
5. Committed and pushed the changes.
6. Learned how Pull Requests are used for reviewing contributions.

## Advantages of Team Collaboration

* Multiple developers can work on one project.
* Changes can be reviewed before merging.
* Git maintains a history of contributions.
* Branches help separate different tasks.
* Collaboration becomes easier to manage.

## Learning Outcome

Learned how to use Git branches, remote repositories, push and pull commands, and Pull Requests for team collaboration.

## Conclusion

Git collaboration helps development teams manage shared projects, review changes, and combine contributions using a structured workflow.
