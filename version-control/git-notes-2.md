---
layout: post
title:  "Notes on Git basics -2, Notes-6"
date:   2016-07-07 10:14:00 -0700
categories: notes, git, github, basics
---

- use `git diff` (without commit ids) to find all changes between current code and previous code in staging area.

- use `git diff --staged` to find code differences between staged and repository
(most recent commits).

- use `git show commithash` to find different between commit and its parent.
*stage area* is code area if you do `git add`
*repository* is code area after `git commit`

- `git reset --hard` to remove all content from staging area and un staged code(working directory).
Only committed code will be present in repository.

- `detached HEAD` is a state where current code base is in an older commit when there are newer commits in repository.
- to get to latest commit, do `git checkout master`
- if changes need to be done for older commit, do `git checkout master`, then make changes, then commit.

#### Branches
- `git branch` shows current Branches. name with * is what current branch is.
- `git branch name` creates branch with name

- use `git checkout branchname` to switch branches

- check **A1** for a short hand for creating and checking out a branch.
- use `git log --graph --oneline branch1 branch 2` to see

**Branches and reachability**
- Every commit has a parent, that is how branching, branch merges work.
- When a commit is made, the HEAD is the pointer that tracks the current commit.
- When you checkout an old commit, the HEAD becomes detached .
- Changes made from old commit code has the old commit as parent, they are usually lost when switched to previous branch.
- to persist the the new commit with the old commit code as parent, you have to create a new branch.

**A1**: Do `git checkout -b new_branch_name`

#### Merging files
* Keep track of base file, and the 2 files to merges
* If content in base file not in 1 merge file, remove content
* if content in 1 merge file not in base file, add content
* if content in 2 merge file but different, manually add content


#### Merging branches
* Merging branches is like creating a new commit with commits from both branches into one.
* Master branch will have the latest commit, `git log` will show all commits sorted by commit time.
* `git log -n 1` shows last 1 commit.
* if branch is deleted before merge, some commits may still be accessible using commit ids.
* They will also become unavailable when git garbage collection runs.
* you can also init garbage collection by `git gc`.

*Git diffs in merged branches*
- It is difficult to find parents while using git logs in merged branches.
- use `git show hashname` to auto-find diff between commit and its parent.

*Merging*
- `git merge` by default merges current branch with mentioned branches.
So always checkout the branch you want to merge and then do merge. Order does not matter. eg. `git merge master coins`

#### Conflict resolution
* Conflicts are noted based on line numbers.
* if `git merge br1 br2` causes merge conflicts, it can be rolled back using git merge --abort.
* else you can checkout conflict files to have <<<HEAD and other demarcations
* once resolution is done, do git add file.
* git will keep track this file was to be merged and suggests `git commit` to merge and does the default merge message
*
