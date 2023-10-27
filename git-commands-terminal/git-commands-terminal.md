# Git Commands in Terminal and Integrated Development Environments (IDEs)

## Introduction
Understanding the basic Git commands is crucial for version control and team collaboration. This guide will introduce you to fundamental Git commands used in the terminal and provide a brief overview of how these commands might be used within various IDEs.

## Terminal Git Commands
**Initializing a Repository**
```bash
git init
```
This command initializes a new Git repository in your current directory.

* **Cloning a Repository**
```bash
git clone [repository_url]
```
   Clone (or download) a repository from an existing URL.

* **Checking the Status of Your Files**
```bash
git status
```
   Shows which changes have been staged, which haven’t, and which files aren’t being tracked.

* **Adding Changes**
```bash
git add [file_name]
```
   To stage all changes, use:
```bash
git add .
```

* **Unstaging Changes**
```bash
git reset HEAD [file_name]
```
This command will unstage the specified file. If you want to unstage all the changes, you can use:
```bash
git reset HEAD .
```
* **Committing Changes**
```bash
git commit -m "Commit message here"
```
Commits your staged content as a new commit snapshot.

* **Pushing Changes to a Remote Repository**
```bash
git push [remote_name] [branch_name]
```
   Typically, `remote_name` is `origin` and branch_name is `main` or `master`.

* **Pulling Changes from a Remote Repository**
```bash
git pull [remote_name] [branch_name]
```

* **Creating a New Branch:**
```bash
git branch [branch_name]
```

* **Switching to a Branch:**
```bash
git checkout [branch_name]
```
**or:**
```bash
git switch [branch_name]
```
* **Deleting a Branch:**
```bash
git branch -d [branch_name]
```

* **To see the list of local branches in your Git repository:**
```bash
git branch
```
* **or remote-tracking branches and local branches at the same time:**
```bash
git branch -a
```

* **Viewing Commit History:**
```bash
git log
```
Displays the commit logs, showing author, date, and commit message. The output is displayed in a reverse chronological order (latest commits first).
To see a more condensed, one-line version of the commit logs with a graph representation, use:
```bash
git log --oneline --graph --all
```


## Git in IDEs
Many modern Integrated Development Environments (IDEs) have built-in support for Git. While the exact methods might differ, the principles are often the same:

1. **Initializing & Cloning Repositories:** Most IDEs have an option to initialize a new repository or clone an existing one, typically found under the File or VCS menu.
2. **Checking File Status:** The IDE will often highlight changed, added, or deleted files in its file explorer or provide a separate panel to view VCS status.
3. **Staging & Committing Changes:** IDEs often provide a panel or window where you can select files to stage and then provide a commit message.
4. **Pushing & Pulling Changes:** IDEs usually have dedicated buttons or menu items to push or pull changes to/from the remote repository.
5. **Branch Management:** You can often switch, create, or merge branches directly within the IDE.

## Conclusion
Both the terminal and modern IDEs offer powerful tools for working with Git. While terminal commands give you fine-grained control and flexibility, IDE integrations can simplify many tasks, especially for those who prefer a graphical interface. Choose the method that aligns best with your comfort level and workflow.
