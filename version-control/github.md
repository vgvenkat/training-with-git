---
layout: post
title:  "Notes on Git basics -1, Notes-5"
date:   2016-07-07 10:14:00 -0700
categories: notes, git, github, basics
---
### Tools to compare files
- Windows : FC (file compare)
- Mac, Linux : DC
  - In mac, go to terminal and do `diff - u file1.html file2.html`


*aside:*
  **Why reflect** - https://sites.google.com/site/reflection4learning/why-reflect
- git repository is just a collection of files
- `git log` to see every commit done. `git log --stat` gives more stats about each commit log.
- `git commit` for every logical change. eg. for change of a color, fixing a bug.
- `git diff` between two commit hashes to find differences.
- `git clone` not only copies files but also commit history.
- `git checkout` to go to a file state on a commit. eg. to check a bug.
Use it with a commit hash.

**For colored diff output**
- `git config --global color.ui auto`

**Git errors**
- `DETACHED HEAD`. If you checkout a commit that is older, the current commit is where the HEAD is pointed will become detached. *What happens if you want to commit to the old-checkout commit? what happens to the head?*

### Git Workspace setup
- Download git-completion.sh, git-prompt.sh
- Download bash_profile and rename it as .bash_profile
- git-completion has auto complete commands, git-prompt has prompt stylings, bash profile has info on how to implement them both.
 ```
  git config --global push.default upstream
  git config --global merge.conflictstyle diff3
  ```
- what does this do?

** The above did not work for me**, I had previously used the iterm bash system given by Wes Bos in his *[commandline](http://wesbos.com/command-line-video-tutorials/)* series.

#### How git works
- Git stores meta-data content in a hidden folder called .git
- All files since creation are tracked here.
- This is how git info is transferred when cloned.

#### Working with a repository
- `git init` creates a git repository by using the hidden .git folder
- git commits are snapshots of code at that time
- `git status` to check how files have changed since last commit

  *Commit Process*
  - current folder => Staging area => repository
        |                  |
         ---- git add ------
  - to remove a mistakenly added file use `git reset`

  *How to write a commit message*
  - [style guide](http://udacity.github.io/git-styleguide/)
  - Use imperative tone while writing commits
  - `git commit -m 'commit message'`
