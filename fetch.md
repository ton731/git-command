### Remote Branches
- `git branch -r`
    - view the remote branches out local repository knows about
- `git checkout origin/master`
    - checkout the remote branch pointer
    - it will go into detached HEAD, don't panic!
- `git switch <remote-branch-name>`
    - create a new local branch from the remote branch of the same name, and track the remote branch origin/branch-name
    - actually, it can also be done with `git checkout --track origin/<remote-branch-name>`


### Fetching
Fetching allows us to download changes from a remote repository, but those changes will not be automatically integrated into our working files.

It lets you see what others have been working on, without haveing to merge those changes into your local repo.

Think of it as "please go and get the latest information from Github, but don't screw up my working directory!"
- `git fetch <remote>`
    - fetches branches and history from a specific remote repository, and it only updates remote tracking branches
- `git fetch <remote> <branch>`
    - fetch a specific branch