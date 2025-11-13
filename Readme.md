# GIT

## What is GIT?

Version contol is also known as source control is the practice of tracking and managing changes to software code

### Architecture of git

There is a 3 states-

- Working Directory
- Staging Area (Index) - waiting area
- Repository (HEAD)

Hashing File contents:When I add a file to git using git add  or commit changes,Git calculate unique SHA-1 hash for the exact content of that file this hash act as a fingerprint . if even a single character in a file changes the hash will be completely different.

The Index (staging Area):Git maintains an "index"(also known as the staging area) which is a snapshot of the files you intend to commit 

Hashing File contents:When I add a file to git using git add  or commit changes,Git calculate unique SHA-1 hash for the exact content of that file this hash act as a fingerprint . if even a single character in a file changes the hash will be completely different.

The Index (staging Area):Git maintains an "index"(also known as the staging area) which is a snapshot of the files you intend to commit 
### GIT MERGE TOOL-

Use git mergetool to run one of several merge utilities to resolve merge conflicts. It is typically run after git merge.

```bash
git mergetool [--tool=<tool>] [-y | --[no-]prompt] [<file>…​]
```
### GIT Stash

```bash
git stash
git stash list
git stash apply
git stash pop
git stash apply stash@{n}
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
git log --oneline 
git log --oneline 
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
### Flow of the branches

we're going to create a develop branch from the main branch 

Feature branches are created from develope and merged back to the develop when finishes

When enough Features are ready, a release branch is created from a develop branch

once the release is stable, release branch is merged into main and develop. main is tagged with a version

If a critical bug is found in production, a hotfix branch is created from main, fixed and merged in to both main and develop

### GIT rev-parse HEAD

git rev - parse HEAD is a command that resolves the HEAD reference to its corresponding commit ID (SHA-1) hash

HEAD - Symbolic reference that points to the currently checkout commit

```bash
git rev-parse HEAD
```

### Atomic Commits	

A fundamental best practice. It means each commit should represent a single, isolated change (e.g., one commit for a bug fix, one for a feature, one for refactoring). This makes history easy to read and reverting/debugging much safer.	

```bash
git add -p (Interactive staging)
```
### GIT reflog

The "safety net." It's a record of where your HEAD has been in your local repository. If you accidentally delete a branch or hard-reset and lose commits, reflog helps you find and recover them.

```bash
git reflog
```

### GIT bisect

A powerful debugging tool that uses a binary search algorithm to automatically find the first commit that introduced a bug, saving hours of manual searching through history.

```bash
git bisect
```

### GIT Hooks 

#### Pre-commit
Run before a commit is finalized most common use is running a linter or formatter

#### commit-msg
Runs after commit message is created.Used to enforce rules for commit message

#### if I create a branch in the local repo, this is how we push that to the remote

```bash
 git push --set-upstream origin test
```
### GIT Add

```bash
git add file_name -to stage sigle specific file 

git add . - to stage all the files in the current directory
```
### Custom commands
This is the value of the alias, enclosed in single quotes. It's the complex part that tells Git to run a shell command sequence.

```bash
'!f() { ... }; f'
```

```bash
git config --global alias.mep '!do_merge _and_push() { git merge "$1" && git push; }; do_merge_and_push'

# Whenever we want to use that command 
git mep test
```
update_test

### GIT revert vs GIT reset

git reset - is a destructive operation that reqrites by removing commits it's best for local, private history cleanup.

git revert is a non-destructive operation that preserves history by creating a brand-new commit that undoes the changes of a prevoius commit.it is safe for public,shared history.

#### Extra - 
git commit -a  -m "New line added" -skip stage environment
git show HEAD - Show the changes introduced in the most recent commit.
git commit -h -show summer for
git branch -d hello-you - to remove branch from the local repo
pull is a combination of: Fetch+Merge
git push --tags -push all local tags to the remote repository
git push origin --delete feature - How to delete a branch named features from the remote 
git switch -c branch-name
git branch -a -list all local and remote branches
git branch -r -list all remote branches
git commit --amend -
git rebase --continue -
git rebase --abort
git checkout -b branch-name abc123 -Restore a deleted branch from a commit hash
*.png - ignore all the files with png extention
.gitarributes -to set file handling riles like line endings, Binary/text. or custom diff
git lfs install -

git LFS-atores pointers on repo file on a storage

git commit -s -m "This is a sign commit" - sign version of the commit
git am 0001-some-change.patch