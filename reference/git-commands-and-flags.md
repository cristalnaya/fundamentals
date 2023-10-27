# Git Flags Reference

This document provides a reference for some of the most commonly used flags in Git.

### `git clone`

- `-b <branch>`: Clone a specific branch.

### `git add`

- `-A` or `--all`: Stage all changes in the entire repository.
- `-u`: Stage only modified and deleted files, but not new files.
- `-p` or `--patch`: Interactively choose hunks of patch to stage.

### `git commit`

- `-m <message>`: Use the given `<message>` as the commit message.
- `-a`: Automatically stage files that have been modified and deleted.
- `--amend`: Modify the most recent commit.
- `-S` or `--gpg-sign`: Sign the commit using GPG.

### `git push`

- `-u` or `--set-upstream`: Set an upstream branch for the current branch.
- `--force` or `-f`: Forcefully push the branch, even if it results in a non-fast-forward merge. Use with caution!
- `--force-with-lease`: Force push, but ensure you do not overwrite someone else's changes. Safer than `--force`.
- `--tags`: Push all tags to the remote repository.

### `git pull`

- `--rebase`: Reapply commits on top of another base tip.
- `--no-rebase`: Merge the upstream changes into the branch.

### `git fetch`

- `--all`: Fetch all remotes.
- `-p` or `--prune`: Prune deleted branches on the remote repository.

### `git branch`

- `-a`: List all branches (local and remote).
- `-r`: List only remote branches.
- `-d <branch>`: Delete a branch (fails if the branch has changes not yet merged).
- `-D <branch>`: Forcefully delete a branch.

### `git checkout`

- `-b <branch>`: Create and switch to a new branch named `<branch>`.
- `-B <branch>`: Create or reset and switch to a branch named `<branch>`.

### `git merge`

- `--no-ff`: Always create a new commit when merging, even if a fast-forward merge is possible.
- `--squash`: Combine all the merge's commit changes into a single commit.

### `git log`

- `--oneline`: Display commits in a short, one-line format.
- `--graph`: Show a text-based graphical representation of the commit history.
- `--all`: Show all branches.
- `-p` or `--patch`: Show the difference introduced in each commit.
- `--stat`: Show stats about changes in each commit (files changed, insertions, deletions).

### `git diff`

- `--staged` or `--cached`: Show the changes that are staged for the next commit.
- `--color`: Show the differences with color (this is usually default behavior).

### `git stash`

- `push`: Save changes that have not been committed to a new stash.
- `pop`: Apply the changes from the most recent stash and remove it.
- `apply`: Apply the changes from a stash, but don't remove the stash.
- `drop`: Remove a stash without applying it.

### `git remote`

- `-v` or `--verbose`: Show the URLs of remote repositories when listing.

### `git clean`

- `-f` or `--force`: Force removal of untracked files.
- `-d`: Remove untracked directories as well.
- `-n` or `--dry-run`: Show what would be removed without actually doing anything.

---

If there are commands or flags not covered in this guide, remember you can always use `git help <command>` for more details.
