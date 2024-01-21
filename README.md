# GitHub Tasks

## Set Your Username and Email in Git Config
```bash
git config --global user.name "<user-name>"
git config --global user.email "<your-email@example.com>"
```
## Create a New Branch and Switch to It
```bash
git checkout -b feature-branch
```
## List All Branches
```bash
git branch
```
## Delete the Branch "feature-branch"
```bash
git branch -d feature-branch
```
## Undo the Last Commit
```bash
git reset HEAD~1
```
## Create a New Branch "conflict-branch"
```bash
git checkout -b conflict-branch
```
## Create Another Branch "feature1"
```bash
git checkout -b feature1
```
## Make Changes in "feature1" Branch and Merge "feature1" Branch into Main
```bash
git checkout main
git merge feature1
```
## Make Changes in "conflict-branch" and Merge main into "conflict-branch"
```bash
git checkout conflict-branch
git merge main
```

*Resolve Merge Conflicts*
```bash
# Follow the prompts to resolve conflicts manually
git add .
git merge --continue
```
## Add a Remote Named "origin" Pointing to a GitHub Repository
```bash
git remote add origin https://github.com/yourusername/your-repo.git
```
## Fork a Repository on GitHub and Clone It
```bash
# Fork the repository on GitHub, then clone it
git clone https://github.com/yourusername/forked-repo.git
```
## Create a New Branch on Your Fork, Make Changes, and Open a Pull Request
```bash
git checkout -b new-feature
# Make changes
git add .
git commit -m "Add new feature"
git push origin new-feature
```
*Comment on a PR and Suggest Improvements*

*Open the Pull Request on GitHub*

*Add comments and suggestions in the GitHub interface*
## Create a Git Alias for git log --oneline Named gitlol
```bash
git config --global alias.gitlol "log --oneline"
```
## Create a Pre-commit Hook
```bash
# Create a file named pre-commit in .git/hooks
# Add your pre-commit script to the file
```
## Handling Urgent Switch to Another Branch without Committing
```bash
# Use stash to save local changes temporarily
git stash
# Switch to the new branch
git checkout new-branch
# Apply the stashed changes back if needed
git stash apply
```
## Restore Deleted File in Local Repository
```bash
git checkout -- path/to/deleted/file
```
## Add File to the Last Commit Without Creating a New Commit
```bash
git add .
git commit --amend --no-edit
```
## Discard All Changes and Revert to the Last Commit
```bash
git reset --hard HEAD
```
## View Changes Introduced by a Specific Commit
```bash
git show commit_hash
```
## Change a Commit Message After Committing
```bash
git commit --amend -m "New commit message"
```
## Incorporate Changes from Another Branch Without Merging
```bash
git checkout your-branch
git cherry-pick other-branch-commit
```
## Squash Multiple Commits into a Single Commit
```bash
git rebase -i HEAD~n
# In the interactive rebase, mark commits as "squash" or "s" to combine them
```
## Unstage a File
```bash
git restore --staged path/to/unwanted/file
```
## Exclude Files with ".yml" Extension and Files Inside "config" Folder from Commit
```bash
# Add to .gitignore:
*.yml
config/
```
## View List of Files Changed in the Last Commit
```bash
git diff --name-only HEAD^ HEAD
```
## Fetch Latest Changes from Remote Without Merging
```bash
git fetch origin branch_name
```
## Recover a Deleted Branch
```bash
git reflog
git checkout -b new-branch recovered_commit_hash
```
## Remove Untracked Files and Directories
```bash
git clean -fd
```
## Apply a Commit from a Feature Branch to Main
```bash
git checkout main
git cherry-pick feature-branch-commit
```
## Apply a Commit to the Correct Branch
```bash
git cherry-pick correct-branch-commit
```
## Cherry-pick a Specific Range of Commits
```bash
git cherry-pick commit_start..commit_end
```
## Clone a GitHub Repository with a Specific Branch
```bash
git clone -b branch_name --single-branch repository_url
```
## Push Local Changes to Your Fork on GitHub
```bash
git push origin your-branch
```
## Create a New Branch Both Locally and on GitHub
```bash
git checkout -b new-feature
git push origin new-feature
```
## View the Commit History of a GitHub Repository
```bash
git log
```
## Remove Sensitive Commit from Local and Remote Repositories
```bash
git revert sensitive-commit-hash
git push origin main
git push origin main --force
```
## Delete a Remote Branch on GitHub
```bash
git push origin --delete branch_name
```