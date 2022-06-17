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