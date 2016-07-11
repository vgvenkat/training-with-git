####Setup osxkeychain for github from terminal
- https://help.github.com/articles/caching-your-github-password-in-git/

#### Setup github remote repository
- remote repository is a hosted version of local repository.
- two ways of interaction is through git pull and push.
- `git remote` shows all remotes present
- `git remote add name` if there are just 1 remote, it is usually named origin.
- so `git remote add origin github_url`

- once remote is set, do `git push origin master` i.e. 2 branches where to push and what to push.
- in github.com, `commits` is similar to `git log`

- `git pull origin master` to pull new contents from

*Fork vs Clone*
- Fork in github gives recognition to original folder creator.(github only)
- clone just makes a copy.

*git pull origin master = git fetch origin + git merge master origin/master*

*Fast forward merge*
- the branch you are merging into must be an ancestor of branch you are merging from.

#### Creating a pull request

- Create a new branch , "pullbranch"
- checkout pullbranch, change files and commit
- `git push origin pullbranch`
- go to github to create a pull request click "new pull request" button.
- verify base branch, write comments for pull request
- It will go to moderator for repository
- Once merged to base branch, the new branch for pull request can be deleted.

- If there are conflicts, pull from origin again and commit to branch, the pull request will also be updated.
- pull request are part of **github**

TODO: Checkout what is upstream when sending pull requests to not-owned repository
