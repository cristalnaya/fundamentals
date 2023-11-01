# Git Basics and Setup
Git is a distributed version control system that helps developers manage and track changes in their codebase over time. This guide will walk you through the basics of Git and how to set it up on your machine.

## What is Git?
Git is a tool that helps multiple people work on the same project at the same time without stepping on each other's toes. It keeps track of changes made to files and allows for merging those changes together. With Git, you can rewind to previous states of a project, work on multiple features at the same time, and even work offline.

## Setting Up Git
1. **Installation**:

* **Windows**: Download and install from [Git for Windows](https://gitforwindows.org/).
* **Mac:** Use Homebrew: `brew install git` or download directly from [Git website](https://git-scm.com/download/mac).
* **Linux:** Use the package manager for your distribution, e.g., `sudo apt-get install git` for Debian/Ubuntu.
2. **Configuration**: After installation, it's a good practice to configure Git with your name and email. This information will be used in your commits.

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```
3. **Check Installation:** Verify that Git was installed correctly:

```bash
git --version
```
or
```bash
git -v
```
## Basic Git Commands

* Initialize a Repository: Start a new repository or reinitialize an existing one.
```bash
git init
```
* **Clone a Repository:** Create a copy of a remote repository on your local machine.
```bash
git clone [repository_url]
```
* **Add Changes:** Track changes in files.
```bash
git add [file-name]
```

To add all changes:
```bash
git add .
```

* **Commit Changes:** Save your changes with a descriptive message.
```bash
git commit -m "Descriptive message here"
```

* **Checking the Status of Your Files**
```bash
git status
```
Shows which changes have been staged, which haven’t, and which files aren’t being tracked.

* To unstage all the changes that have been staged:
```bash
git reset
```

* **Unstaging Changes**
```bash
git reset HEAD [file_name]
```
This command will unstage the specified file. If you want to unstage all the changes, you can use:
```bash
git reset HEAD .
```

**Push Changes:** Send your committed changes to a remote repository.
```bash
git push [remote-name] [branch-name]
```
* **Pull Changes:** Fetch and merge changes from a remote repository.

```bash
git pull [remote-name] [branch-name]
```
* **View Log:** See a history of commits.

```bash
git log
```
Displays the commit logs, showing author, date, and commit message. The output is displayed in a reverse chronological order (latest commits first).

To see a more condensed, one-line version of the commit logs with a graph representation, use:
```bash
git log --oneline --graph --all
```

* Checking the Changes in a Specific Commit
```bash
git show [commit_id]
```
Displays the changes made in a specific commit. Replace `[commit_id]` with the commit's SHA-1 hash. This command will show the diff along with the commit message.

## Conclusion
Git is a powerful tool for version control, collaboration, and code management. While there's much more to learn, mastering the basics sets you on a path to becoming a proficient Git user.
