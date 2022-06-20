### Pull
Git pull is another command we can use to retrieve changes from a remote repository. Unlike fetch, pull actually updates our HEAD branch with whatever changes are retrieved from the remote.

Think of it as "go and download data from Github AND immediately update my local repo with those changes".

**git pull = git fetch + git merge**

- `git pull <remote> <branch>`
    - fetch the lastest information from the origin's master branch and merge those changes into our current branch
    - conflicts may occur when there are conflict between remote file content and those in local
- `git pull`
    - remote will default to origin
    - branch will default to whatever tracking connection is configured for your current branch


### Git Fetch vs. Git Pull
- `git fetch`
    - gets changes from remote branch(es)
    - updates the remote-tracking branches with the new changes
    - does not merge changes onto your current HEAD branch
    - safe to do at anytime
- `git pull`
    - gets changes form remote branch(es)
    - updates the current branch with the new changes merging them in
    - can result in merge conflict
    - **Not recommended if you have uncommitted changes!**