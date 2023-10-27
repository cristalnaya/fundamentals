# Git Basics and Setup
Git is a distributed version control system that helps developers manage and track changes in their codebase over time. This guide will walk you through the basics of Git and how to set it up on your machine.

## What is Git?
Git is a tool that helps multiple people work on the same project at the same time without stepping on each other's toes. It keeps track of changes made to files and allows for merging those changes together. With Git, you can rewind to previous states of a project, work on multiple features at the same time, and even work offline.

## Setting Up Git
1. Installation:

* **Windows**: Download and install from Git for Windows.
* **Mac:** Use Homebrew: brew install git or download directly from Git website.
* **Linux:** Use the package manager for your distribution, e.g., sudo apt-get install git for Debian/Ubuntu.
2. **Configuration**: After installation, it's a good practice to configure Git with your name and email. This information will be used in your commits.

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```
3. **Check Installation:** Verify that Git was installed correctly:

```bash
git --version
```
## Basic Git Commands
* Initialize a Repository: Start a new repository or reinitialize an existing one.

```bash
git init
```
* **Clone a Repository:** Create a copy of a remote repository on your local machine.
```bash
git clone [URL]
```
* **Add Changes:** Track changes in files.

bash
git add [file-name]
To add all changes:

```bash
git add .
```

* **Commit Changes:** Save your changes with a descriptive message.

```bash
git commit -m "Descriptive message here"
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

## Git Workflows
Understanding Git's basic commands is crucial, but effectively using Git requires understanding workflows like:

* **Feature branching:** Keeping different features in separate branches.
* **Gitflow:** A specific set of guidelines for using feature, develop, and master branches.
* **Forking:** Copying a remote repository to create a distinct project.

## Conclusion
Git is a powerful tool for version control, collaboration, and code management. While there's much more to learn, mastering the basics sets you on a path to becoming a proficient Git user.

