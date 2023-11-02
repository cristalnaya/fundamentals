# Advanced Command Workflows

## Branch Management
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

* To create and switch to a new branch in one command:
```bash
 git checkout -b [branch_name]
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

* **Merging Branches**
When you feel your feature or fix is ready, it's time to merge it back to the main branch.

  * **Fast-Forward Merge:** If the main branch hasn't seen any new snapshots since you started your feature branch, Git simply moves the main branch pointer forward.

  * **3-Way Merge:** If there have been new snapshots in the main branch, Git will create a new snapshot that results from this three-way merge and automatically creates a new commit that points to it.

```bash
git merge [branch-name]
```

## Managing Changes
### **Fetching Changes**
Fetching is an essential part of using Git, especially when you're working with others. Here's what git fetch does:
* **Updates Your Local References:** It gets the latest references (like commits, files, and refs) from the remote repository without merging them into your current branch. This means you can see what others have done without combining their work with yours just yet.
* **Safe for Local Changes:** git fetch is a non-destructive operation. It won't change any of your current working files or local branches. It's safe to do at any time to ensure you have the latest data from the remote. 
* **Preparation for Merging:** After fetching, you can use git merge or git rebase to combine the fetched changes into your branch when you're ready.
```bash
git fetch [remote_name]
```
For example, if you're working on a feature branch and want to check if there have been updates to the main branch without affecting your current work, you can run:
```bash
git fetch origin main
```
This command updates your local copy of the main branch, but it doesn't merge any changes into your feature branch. Now you can decide to merge these updates into your feature branch whenever it's convenient.

Remember, this command doesn't change your working directory. It only updates the information your local repository has about the remote.

### Stash changes
* When you need to switch branches but don't want to commit your changes yet:
```bash
git stash
```

* To apply stashed changes:
```bash
git stash apply
```
### **Viewing Commit History:**
```bash
git log
```
Displays the commit logs, showing author, date, and commit message. The output is displayed in a reverse chronological order (latest commits first).

## Rebasing and Resolving Conflicts
1. **Rebasing with another branch**
When you want to incorporate the latest changes from another branch into your feature branch without merging, you can use rebase. This helps in maintaining a cleaner, linear history.

**Note:** Before rebasing, it's good practice to ensure you have the latest updates from the branch you want to rebase onto. Typically, the [branch-name] will be `master` or `main` if you are rebasing your feature branch to ensure it's up-to-date with the main line of development.

Here's how you can do it:
* Update the branch you want to rebase onto:
```bash
git checkout [branch-name]
git pull
```

* Switch to your feature branch:
```bash
git checkout [your-feature-branch]
```

* Start the rebase:
```bash
git rebase [branch-name]
```
Remember, if you encounter merge conflicts during rebasing, you'll need to resolve them. Once resolved, you can continue the rebase with `git rebase --continue`.

2. Resolving Merge Conflicts:
* **Manual Edit:** Open the conflicted file in a text editor or IDE. Decide which version of the conflict you'd like to keep or if you'd like to combine them. Remove the conflict markers (<<<<<<<, =======, and >>>>>>>) and edit the file until you're satisfied with the content.

* **Using a Merge Tool:** If you're using an IDE or have a merge tool configured, you can use commands like `git mergetool` to invoke a visual interface to help resolve the conflicts.

## Completing the Merge or Rebase:
* **For Merges:** After resolving the conflict in the file:
```bash 
git add [resolved-file-name]
git commit
```
This will create a new merge commit. The default commit message will indicate it's a merge, but you can edit it if needed.

* **For Rebases:** After resolving the conflict:
```bash
git add [resolved-file-name]
git rebase --continue 
```
This will continue the rebase process. If there are more conflicts in subsequent commits, you'll need to resolve them in a similar manner until the rebase is complete.

## Best Practices and Tips
* **Always Pull Latest:** Before merging or rebasing, always pull the latest changes from the target branch.
* **Atomic Commits:** Making atomic commits, i.e., small commits that focus on a single logical change, can reduce the likelihood and complexity of conflicts.
* **Frequent Merges/Rebases:** If working on a long-lived branch, consider merging from the main branch or rebasing frequently. This will reduce the chances of large, complicated conflicts.
* **Communicate:** If collaborating on a feature with others, communicate about changes and merges to avoid unnecessary conflicts.
* **Backup:** Before doing a complex merge or rebase, consider creating a backup branch. This gives you a safety net to return to if things go awry.

## Git in IDEs
Many modern Integrated Development Environments (IDEs) seamlessly integrate Git functionalities, enhancing the coding workflow. IDEs like **Visual Studio Code (VS Code)**, **IntelliJ IDEA**, **Eclipse**, and **Atom** are just a few examples that offer this support. Delving deeper:

* **Initializing & Cloning Repositories:** Most IDEs have an option to initialize a new repository or clone an existing one, typically found under the File or VCS menu.
* **Checking File Status:** The IDE will often highlight changed, added, or deleted files in its file explorer or provide a separate panel to view VCS status.
* **Staging & Committing Changes:** IDEs often provide a panel or window where you can select files to stage and then provide a commit message.
* **Pushing & Pulling Changes:** IDEs usually have dedicated buttons or menu items to push or pull changes to/from the remote repository.
* **Branch Management:** You can often switch, create, or merge branches directly within the IDE.

## Conclusion
Advanced Git techniques, combined with the capabilities of modern IDEs, enable more streamlined workflows and enhanced codebase management. Whether you're working solo or in a team, mastering these skills will contribute to a smoother development process.
