### Detached HEAD (It's not a bad thing!)
- `git checkout <commit-hash>`
    - You have a couple options:
        1. stay in detached HEAD to examine the contents of old commit
        2. leave and go back to wherever you were before - reattach the HEAD
        3. create a new branch and switch to it, then can now make and save changes, since HEAD is no longer detached
- `git checkout HEAD~2`
    - go back to the commit, where HEAD~2 refers to 2 commits before HEAD
- `git switch -`
    - go back to last branch


### Discard Changes with Git Checkout
- `git checkout HEAD <file-name>`
    - discard the changes and revert back to whatever it looked like when you last committed
- `git checkout -- <file-name>`
    - same as `git checkout HEAD <file-name>`


### Unmodifiying Files with Restore
- `git restore <file-name>`
    - to restore the file to the content in the HEAD
- `git restore --source HEAD~2 <file-name>`
    - to restore the file to the given source


### Unstaging Files with Git Restore
- `git restore --staged <file-name>`
    - remove the file from staging


### Git Reset
- `git reset <commit-hash>`
    - reset the repo back to a specific commit
    - the commits after the given commit will be deleted, but the changes of the files will be remained as unstaged
- `git reset --hard <commit-hash>`
    - delete the last commit and the associated changes