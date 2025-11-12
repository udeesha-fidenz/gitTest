# GIT

## What is GIT?

Version contol is also known as source control is the practice of tracking and managing changes to software code

### GIT MERGE TOOL-

Use git mergetool to run one of several merge utilities to resolve merge conflicts. It is typically run after git merge.

```bash
git mergetool [--tool=<tool>] [-y | --[no-]prompt] [<file>…​]
```
## GIT Stash

```bash
git stash
git stash list
git stash apply
```
### GIT remove rm

```bash
git remote rm origin
```

### GIT Remote

```bash
git add remote hehe
```
### GIT SVN

bidirectional operations between a single Subversion tree and git 

```bash
git svn
```
### GIT Log

```bash
git log
```
### GIT Rebase

This fetches revisions from the SVN parent of the current HEAD and rebases the current (uncommitted to SVN) work against it.

```bash
git rebase
```
### GIT Grep <Text need to search>

```bash
git grep hello
```

### GIT Abort Merge

```bash
use "git merge --abort" to abort the merge
```
### GIT branch delete 

```bash
git branch -d branch name 
```
### GITK-gitk - The Git repository browser

```bash
 gitk HEAD..FETCH_HEAD
 ```
### GIT Restore

```bash
git restore
```

### GIT Tag

```bash
git tag
```

### GIT Reset 

git Reset is a powerfull command used to undo changes by moving the current branch HEAD pointer to specific commit

Used to Unstage files
Undo recent commits
Discard all local changes and return the repository to a clean state matching the last commit(git reset --hard HEAD)

```bash
git reset --soft Head
git reset --hard
git reset --mixed
```
### GIT Rebase

git rebase is a powerful command for integrating changes from one branch into another, offering a cleaner, linear project history compared to a standard git merge. It essentially moves or combines a sequence of commits to a new base commit.

Interactive Rebase (git rebase -i) 

```bash
git rebase -i
--------------------------------------
git rebase -i HEAD~<number-of-commits>
or
git rebase -i <commit-hash>
--------------------------------------
```