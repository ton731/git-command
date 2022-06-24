### Rebase
There are two main ways to use the git rebase command:
1. as an alternative to merging
2. as a cleanup tool

### 1. 
- Instead of using a merge commit, rebasing rewrites history by creating new commits for each of the original feature branch commit.
- We can also wait until we are done with a feature and then rebase the feature branch onto the master branch.
- Rebase can help you get a clean and clear linear history without unnecessary merge commits.
    ```
    git switch feature
    git rebase main
    ```

### **Warning!**
- Never rebase commits that have been shared with others. If you have already push commits up to Github, **DO NOT** rebase them unless you are positive no one on the team is using those commits.

### **Seriously**
You do not want to rewrite and git history that other people already have. It's a pain to reconcile the alternate histories!