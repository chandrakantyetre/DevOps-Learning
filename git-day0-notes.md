# Day 0 – Git & GitHub Repository Management Notes

## Objective

Understand Git, GitHub, repositories, repository management, and SSH authentication before starting the DevOps bootcamp.

---

# 1. What is Git?

Git is a **Distributed Version Control System (DVCS)** used to track changes in files and source code.

### Why Git?

* Tracks every change made to files.
* Maintains complete version history.
* Enables collaboration among multiple developers.
* Allows reverting to previous versions if needed.
* Forms the foundation of modern DevOps and CI/CD workflows.

---

# 2. What is GitHub?

GitHub is a cloud-based platform that hosts Git repositories.

### Uses of GitHub

* Store code online.
* Backup projects.
* Collaborate with teams.
* Review code changes.
* Integrate with CI/CD tools like Jenkins and GitHub Actions.

---

# 3. What is a Repository?

A repository (repo) is a project folder managed by Git.

It stores:

* Source code
* Documentation
* Images
* Configuration files
* Scripts
* Complete history of changes

---

# 4. Local Repository vs Remote Repository

## Local Repository

Stored on your computer or EC2 instance.

Example:

```text
/home/ubuntu/DevOps-Learning
```

This is where you edit files.

---

## Remote Repository

Stored on GitHub.

Example:

```text
GitHub
    │
DevOps-Learning Repository
```

Used for backup and collaboration.

---

# 5. Repository Structure

Example:

```text
DevOps-Learning/
│
├── README.md
├── Linux/
│   ├── Notes.md
│   ├── Commands.md
│   └── Labs/
│
├── Networking/
│   ├── Notes.md
│   └── Images/
│
├── Git/
├── Docker/
├── Jenkins/
├── Maven/
├── AWS/
├── Kubernetes/
├── Terraform/
├── Ansible/
├── Monitoring/
└── Projects/
```

Keep every topic in a separate folder.

---

# 6. What is README.md?

`README.md` is the first document people see when they open a repository.

GitHub automatically displays it on the repository home page.

Typical contents:

* Project overview
* Objectives
* Features
* Installation steps
* Technologies used
* Author information

---

# 7. What is Markdown (.md)?

`.md` stands for **Markdown**.

Markdown is a lightweight markup language used to create formatted documents.

Example:

```markdown
# DevOps Learning

## Technologies

- Linux
- Docker
- Jenkins
```

GitHub renders Markdown into a nicely formatted web page.

---

# 8. Daily Git Workflow

```text
Edit Files
     ↓
git status
     ↓
git add .
     ↓
git commit -m "Meaningful message"
     ↓
git push origin main
```

---

# 9. Important Git Commands

## Check repository status

```bash
git status
```

Displays modified, new, or deleted files.

---

## Stage files

Add everything:

```bash
git add .
```

Add a specific file:

```bash
git add README.md
```

---

## Commit changes

```bash
git commit -m "Added Linux notes"
```

A commit is a snapshot of your project at a specific point in time.

---

## Push changes

```bash
git push origin main
```

Uploads commits to GitHub.

---

## Download latest changes

```bash
git pull origin main
```

---

## Clone repository

Using HTTPS:

```bash
git clone https://github.com/<username>/DevOps-Learning.git
```

Using SSH (recommended):

```bash
git clone git@github.com:<username>/DevOps-Learning.git
```

---

# 10. Why Did HTTPS Authentication Fail?

Error received:

```text
Password authentication is not supported for Git operations.
```

Reason:

GitHub no longer allows account passwords for Git operations over HTTPS.

Supported authentication methods:

* SSH Keys (Recommended)
* Personal Access Token (PAT)

---

# 11. Why Use SSH?

Advantages:

* More secure than passwords.
* No need to enter credentials repeatedly.
* Industry-standard authentication.
* Used with GitHub, GitLab, EC2, Jenkins, and many Linux servers.

---

# 12. Creating an SSH Key

Command:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

This creates two files:

```text
~/.ssh/id_ed25519
~/.ssh/id_ed25519.pub
```

---

# 13. Public Key vs Private Key

## Private Key

File:

```text
id_ed25519
```

* Secret
* Never share it
* Never upload it to GitHub
* Used to prove your identity

---

## Public Key

File:

```text
id_ed25519.pub
```

* Safe to share
* Upload to GitHub
* Used by GitHub to verify your identity

---

# 14. How SSH Authentication Works

```text
EC2 Instance
     │
Private Key
     │
     ▼
Internet
     │
     ▼
GitHub
     │
Public Key
```

Authentication process:

1. GitHub stores your public key.
2. Your EC2 uses the matching private key.
3. GitHub verifies the key pair.
4. Access is granted without a password.

---

# 15. What is authorized_keys?

Current contents of:

```text
~/.ssh/
```

Initially:

```text
authorized_keys
```

This file allows users to **log in to your EC2 instance**.

It is **not** used to authenticate your EC2 instance with GitHub.

---

# 16. Why Use ED25519?

Command:

```bash
ssh-keygen -t ed25519
```

Advantages:

* Modern cryptography
* Fast authentication
* Strong security
* Smaller key size
* Recommended by GitHub

---

# 17. Other SSH Key Algorithms

| Algorithm | Command                     | Status                 |
| --------- | --------------------------- | ---------------------- |
| RSA       | `ssh-keygen -t rsa -b 4096` | Supported, widely used |
| ED25519   | `ssh-keygen -t ed25519`     | Recommended            |
| ECDSA     | `ssh-keygen -t ecdsa`       | Supported              |
| DSA       | `ssh-keygen -t dsa`         | Obsolete               |

---

# 18. What Does "25519" Mean?

It is **not** the key size.

ED25519 uses **Curve25519**, a modern elliptic curve used in cryptography.

The name refers to the algorithm, not a configurable number.

---

# 19. Professional DevOps Workflow

```text
Windows
    │
SSH
    │
EC2 (Ubuntu)
    │
Git Commands
    │
GitHub Repository
```

This is a common workflow used by DevOps engineers.

---

# 20. Best Practices

* Keep repositories well organized.
* Write meaningful commit messages.
* Commit small, logical changes.
* Push work regularly.
* Never commit passwords, private keys, or secrets.
* Use SSH instead of HTTPS for authentication.
* Document your work with Markdown.

---

# Interview Questions

### Q1. What is Git?

Git is a distributed version control system used to track changes in files and enable collaboration.

---

### Q2. What is GitHub?

GitHub is a cloud platform that hosts Git repositories and supports collaboration, version control, and CI/CD integration.

---

### Q3. What is the difference between Git and GitHub?

* Git is the version control software.
* GitHub is an online platform that hosts Git repositories.

---

### Q4. What is a repository?

A repository is a project folder managed by Git that stores files, folders, and the complete history of changes.

---

### Q5. What is README.md?

A Markdown document that describes the project. GitHub automatically displays it on the repository home page.

---

### Q6. What is the difference between a local repository and a remote repository?

* Local repository: Stored on your machine for development.
* Remote repository: Stored on GitHub for backup and collaboration.

---

### Q7. Why is SSH preferred over HTTPS?

SSH provides secure, passwordless authentication using public and private keys, making it the preferred method in professional environments.

---

### Q8. What is the difference between a public key and a private key?

* Public key: Shared with servers like GitHub.
* Private key: Kept secret on your machine and used to prove your identity.

---

### Q9. Why do we use ED25519?

ED25519 is recommended because it offers strong security, faster authentication, and smaller keys compared to older algorithms.

---

## Day 0 Summary

Today I learned:

* Git fundamentals
* GitHub fundamentals
* Repository management
* Markdown (`.md`) files
* Local vs Remote repositories
* Common Git commands
* SSH authentication
* Public and Private keys
* ED25519 SSH keys
* Professional GitHub workflow used by DevOps engineers

**Status:** Day 0 Completed ✅

