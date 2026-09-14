## 1. Introduction to GitLab

GitLab is a web-based DevOps platform used for software development, version control, collaboration, and CI/CD.

It provides developers with a single platform where they can write code, store source code, track issues, review code, and automate software testing and deployment.

GitLab uses Git as its underlying version control system.

### Simple Example

A development team is creating a website.

* Developer 1 writes the frontend code.
* Developer 2 writes the backend code.
* Both developers store their code in a GitLab repository.
* They create branches for their work.
* After completing their work, they create a Merge Request.
* The team reviews the code.
* GitLab CI/CD can automatically test the code.
* If the tests are successful, the application can be deployed.

Therefore, GitLab helps manage the complete software development process.

---

## 2. What is GitLab?

**GitLab is a DevOps platform that provides Git-based source code management along with tools for collaboration, CI/CD, issue tracking, code review, and deployment.**

GitLab allows developers to manage their complete software development lifecycle from one platform.

### Main Uses of GitLab

1. Source code management
2. Version control
3. Team collaboration
4. Branch management
5. Code review
6. Issue tracking
7. Continuous Integration
8. Continuous Delivery/Deployment
9. Automated testing
10. Application deployment

---

## 3. GitLab Features

### 1. Version Control

GitLab uses Git to maintain different versions of source code.

Developers can see changes made to the project and return to previous versions when required.

### 2. Repository

A repository stores the project's source code and related files.

### 3. Branching

Developers can create separate branches to work on different features without directly changing the main code.

### 4. Merge Requests

Merge Requests are used to propose changes from one branch to another.

They also allow team members to review code before merging it.

### 5. Issue Tracking

GitLab Issues help teams report bugs, create tasks, and track project work.

### 6. CI/CD

GitLab provides tools to automatically build, test, and deploy applications.

### 7. Collaboration

Multiple developers can work on the same project and communicate through issues, merge requests, and discussions.

### 8. Security

GitLab provides security features for source code, applications, and development workflows.

---

## 4. Git vs GitLab

| Git                                      | GitLab                                                       |
| ---------------------------------------- | ------------------------------------------------------------ |
| Git is a version control system.         | GitLab is a DevOps platform.                                 |
| Mainly manages source code versions.     | Provides source code management plus DevOps features.        |
| Usually works through commands.          | Provides a web interface as well as Git functionality.       |
| Can work locally.                        | Commonly used as a remote collaboration platform.            |
| Created for distributed version control. | Built around Git and provides collaboration and CI/CD tools. |

### Simple Way to Remember

**Git = Tool for version control**

**GitLab = Platform that uses Git + provides DevOps features**

---

## 5. GitLab Project

A GitLab Project is a workspace where a software project is managed.

A project can contain:

* Source code
* Repository
* Branches
* Issues
* Merge Requests
* CI/CD pipelines
* Documentation
* Project settings

For example, a project named `student-management-system` can contain all the code and development activities related to that application.

---

## 6. GitLab Repository

A repository is a storage location for project files and their version history.

It contains:

* Source code
* Files
* Folders
* Commit history
* Branches

The repository allows developers to track how the project changes over time.

---

## 7. GitLab Branch

A branch is a separate line of development in a Git repository.

Branches allow developers to work on different features without directly modifying the main branch.

### Example

Suppose the main branch contains the stable project.

A developer wants to create a login feature.

They can create:

```bash
git checkout -b login-feature
```

The developer works on the login feature in this branch.

After completing the work, the branch can be merged into the main branch through a Merge Request.

---

## 8. Commit

A commit is a saved record of changes made to files in a Git repository.

### Example

```bash
git add .
git commit -m "Added login page"
```

The commit message describes what changes were made.

### Importance of Commit

* Saves changes
* Maintains project history
* Helps identify changes
* Makes collaboration easier
* Allows previous versions to be tracked

---

## 9. Push and Pull

### Push

`git push` uploads local commits to a remote repository such as GitLab.

```bash
git push origin main
```

### Pull

`git pull` downloads the latest changes from the remote repository and updates the local repository.

```bash
git pull origin main
```

### Simple Flow

```text
Local Repository
       |
     Push
       ↓
GitLab Repository
       |
     Pull
       ↓
Local Repository
```

---

## 10. Merge Request

A **Merge Request (MR)** is a request to merge changes from one branch into another branch.

For example:

```text
feature-login
      ↓
Merge Request
      ↓
main
```

Before merging, team members can:

* Review the code
* Discuss changes
* Suggest modifications
* Run automated tests
* Approve the changes

Merge Requests are therefore an important part of collaborative development.

---

## 11. GitLab Issues

GitLab Issues are used to track project tasks, bugs, requirements, and other work.

### Example

If a website has a broken login button, a developer can create an issue:

```text
Issue: Login button is not working
```

The issue can be assigned to a team member and tracked until it is completed.

---

## 12. GitLab CI/CD

CI/CD is one of the most important features of GitLab.

### CI – Continuous Integration

Continuous Integration means automatically building and testing code whenever developers make changes.

### CD – Continuous Delivery / Continuous Deployment

Continuous Delivery or Deployment automates the process of delivering or deploying the application.

### Simple Flow

```text
Developer writes code
        ↓
      Commit
        ↓
       Push
        ↓
GitLab Pipeline starts
        ↓
      Build
        ↓
      Test
        ↓
     Deploy
```

This reduces manual work and helps detect errors early.

---

## 13. GitLab Pipeline

A pipeline is a collection of automated processes that run when changes are pushed to the repository.

A typical pipeline may contain:

```text
Build → Test → Deploy
```

For example:

```text
Build Stage
     ↓
Test Stage
     ↓
Deploy Stage
```

If a test fails, the pipeline can stop and prevent incorrect code from being deployed.

---

## 14. Jobs and Stages

### Job

A job is a specific task performed by GitLab CI/CD.

Examples:

* Compile code
* Run tests
* Build application
* Deploy application

### Stage

A stage is a group or phase containing one or more jobs.

Example:

```text
Stages:

1. Build
2. Test
3. Deploy
```

Each stage can contain multiple jobs.

---

## 15. `.gitlab-ci.yml`

The `.gitlab-ci.yml` file is a configuration file used to define the GitLab CI/CD pipeline.

It is normally placed in the root directory of the repository.

### Example

```yaml
stages:
  - build
  - test

build_job:
  stage: build
  script:
    - echo "Building application"

test_job:
  stage: test
  script:
    - echo "Running tests"
```

Here:

* `stages` defines pipeline stages.
* `build_job` is a build job.
* `test_job` is a testing job.
* `script` contains commands executed by the job.

---

## 16. GitLab Runner

A **GitLab Runner** is an application that executes CI/CD jobs.

When a GitLab pipeline starts, the Runner receives the job and executes the commands defined in the CI/CD configuration.

### Simple Flow

```text
GitLab
   ↓
Pipeline
   ↓
Job
   ↓
GitLab Runner
   ↓
Command Execution
   ↓
Result
```

The Runner can execute tasks such as:

* Building applications
* Running tests
* Creating packages
* Deploying applications

---

## 17. GitLab CI/CD Workflow

The basic GitLab CI/CD workflow is:

```text
Developer
    ↓
Write Code
    ↓
Commit
    ↓
Push to GitLab
    ↓
Pipeline Starts
    ↓
Build
    ↓
Test
    ↓
Deploy
```

This automation helps organizations deliver software faster and more reliably.

---

## 18. Advantages of GitLab

1. Provides Git-based version control.
2. Supports team collaboration.
3. Provides code

