### Remote
Before we can push anything up to Github, we need to tell git about our remote repository on Github. We need to set up a "destination" to push up to.
In Git, we refer to these destinations as remotes. Each remote is simply a URL where a hosted repository lives.
- `git remote`
    - `-v` for verbose, more info
    - view existing remotes for the repository
- `git remote add <name> <url>`
    - adding a new remote
    - usually the name will be "origin", it's a conventional Git remote name

Not commonly used
- `git remote rename <old> <new>`
- `git remote remove <name>`


### Push
- `git push <remote> <branch>`
    - after a remote is set up, we can push our work to Github
    - for example, `git push origin master`