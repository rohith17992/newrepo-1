Git Commands
============ 
_Forked from [@joshnh «A list of my commonly used Git commands»](https://github.com/joshnh/Git-Commands)_  

*If you are interested in Josh's Git aliases, have a look at [`.bash_profile`](https://github.com/joshnh/bash_profile/blob/master/.bash_profile)*


### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Creating a new repository from command line ###

| Command |
| ------- |
|`echo "# [repository-name]" >> README.md`|
|`git init`|
|`git add README.md`|
|`git commit -m "first commit"`|
|`git remote add origin https://github.com/[username]/[repository-name].git`|
|`git push -u origin master`|

### Connect to a remote repository

| Command | Description |
| ------- | ----------- |
| `git remote add origin [server]` | Connect your local repository to a remote server |
| `git remote -v` | List all configured remote repositories |

### Configuring a remote for a fork and syncing a fork
| Command | Description |
| ------- | ----------- |
| `git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git` | Specify a new remote upstream repository that will be synced with the fork |
| `git remote -v`| Verify the new upstream repository you've specified for your fork |
| `git fetch upstream` | Fetch the branches and their respective commits from the upstream repository. Commits to `master` will be stored in a local branch, `upstream/master` |
| `git checkout master` | Check out your fork's local `master` branch |
| `git merge upstream/master` | Merge the changes from `upstream/master` into your local `master` branch. This brings your fork's `master` branch into sync with the upstream repository, without losing your local changes |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -f branch-name [new-tip-commit_ID]` | Move branch pointer to new/different commit |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branchName]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and set an upstream, remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin -f` | Gorces push onto specific branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |
| `git config --global user.email "email@example.com"` | Setting your email address for every repository on your computer |
| `git config user.email "email@example.com"` | Setting your email address for a single repository on your computer |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git diff [source branch] [target branch}` | Preview changes before merging |

### README syntax

https://help.github.com/articles/basic-writing-and-formatting-syntax/#styling-text
