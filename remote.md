### Remote
Before we can push anything up to Github, we need to tell git about our remote repository on Github. We need to set up a "destination" to push up to.
In Git, we refer to these destinations as remotes. Each remote is simply a URL where a hosted repository lives.
- `git remote`
    - `-v` for verbose, more info
    - view existing remotes for the repository
- `git remote add <name> <url>`
    - connect your local repo to the remote 
    - usually the name will be "origin", it's a conventional Git remote name

Not commonly used
- `git remote rename <old> <new>`
- `git remote remove <name>`


### Push
- `git push <remote> <branch>`
    - after a remote is set up, we can push our work to Github
    - for example, `git push origin master`
- `git push <remote> <local-branch>:<remote:branch>`
    - not very common
    - for example, `git push origin test_func_branch:master`
- `git push -u <remote> <branch>`
    - set the upstream of the branch we are pushing
    - a link to connect our local branch to a Github branch
    - for example, `git push -u origin master`, after this setting, in the master branch, we can only use `git push` to push the master branch to the remote