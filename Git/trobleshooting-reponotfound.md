# Git Troubleshooting Notes – "Repository not found" Error

## Error

While cloning a GitHub repository using SSH:

```bash
git clone git@github.com:DevOps-Learning
```

Output:

```text
Cloning into 'DevOps-Learning'...
ERROR: Repository not found.
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```

---

# Why Does This Error Occur?

This error usually means GitHub cannot locate the repository or you don't have permission to access it.

It **does not always mean that SSH is broken.**

---

# Common Causes

## 1. Incorrect Repository URL (Most Common)

### Wrong

```bash
git clone git@github.com:DevOps-Learning
```

Problem:

* GitHub username is missing.
* Repository name alone is not enough.

### Correct Format

```bash
git clone git@github.com:<github-username>/<repository-name>.git
```

Example:

```bash
git clone git@github.com:yetrechandrakant/DevOps-Learning.git
```

---

## 2. Repository Does Not Exist

The repository may:

* Not have been created.
* Have been deleted.
* Have been renamed.

Verify by opening the repository in your browser.

---

## 3. Wrong GitHub Username

Example:

Repository owner:

```text
yetrechandrakant
```

But clone command:

```text
git@github.com:chandrakant/DevOps-Learning.git
```

This results in:

```text
Repository not found.
```

Always verify the repository owner's username.

---

## 4. Repository is Private

If the repository is private:

* You must have permission to access it.
* Your GitHub account must be authorized.

---

## 5. SSH Authentication Not Configured

Before cloning, verify SSH authentication.

Run:

```bash
ssh -T git@github.com
```

Expected output:

```text
Hi <your-github-username>! You've successfully authenticated, but GitHub does not provide shell access.
```

If authentication fails, configure SSH keys first.

---

# Correct Troubleshooting Procedure

## Step 1

Test SSH connection.

```bash
ssh -T git@github.com
```

---

## Step 2

Copy the repository URL from GitHub.

GitHub → Repository → **Code** → **SSH**

Example:

```text
git@github.com:yetrechandrakant/DevOps-Learning.git
```

Never type the URL manually if you can copy it.

---

## Step 3

Clone the repository.

```bash
git clone git@github.com:yetrechandrakant/DevOps-Learning.git
```

---

# Repository URL Structure

```text
git@github.com:
        │
        ├── GitHub Username
        │
        ├── /
        │
        ├── Repository Name
        │
        └── .git
```

Example:

```text
git@github.com:yetrechandrakant/DevOps-Learning.git
```

---

# Interview Question

### Q. What does the "Repository not found" error mean?

**Answer:**

This error means GitHub cannot locate the requested repository or the user does not have permission to access it. Common causes include an incorrect repository URL, incorrect GitHub username, a deleted or private repository, or insufficient access rights.

---

# Troubleshooting Checklist

When you see:

```text
Repository not found
```

Check the following:

* Is the repository name correct?
* Is the GitHub username correct?
* Does the repository exist?
* Is the repository private?
* Are you using the correct SSH URL?
* Does `ssh -T git@github.com` authenticate successfully?

---

# Key Learning

The message **"Repository not found"** does **not** automatically indicate an SSH problem. Always verify the repository URL and access permissions before troubleshooting SSH.

