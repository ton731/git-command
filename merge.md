### Fast Forward Merge
- When the master merge didn't commit since creating the new branch, and the new branch want to merge back into the master branch. The Fast-Forward-Merge just simply move the HEAD from master to the new branch.
- There are two steps, switch to the main branch and merge:
    1. `git switch master`
    2. `git merge new-branch`


### Merge (sometimes with Conflicts)
- When both the main branch and the new branch commit, and you want to merge the new branch into the main branch, it may cause some conflicts. There are a few steps:
    1. `git switch master`, and `git merge new-branch`
    2. resolve the conflict markers in the text editor, devide which to keep
    3. add your changes and make a commit