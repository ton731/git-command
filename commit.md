### Add (Stage)
- `git add <file_name>...`
- `git add .`
    - stage all files
- `git restore --staged file_name` or `git reset -- file_name`
    - will unstage any staged changes for the given file(s)
- `git rm --cached file_name `
    - does not unstage a file, it actually stages the removal of the file(s) from the repo (assuming it was already committed before) but leaves the file in your working tree (leaving you with an untracked file)

### Commit
- `git commit`
    - it will open vim defaultly
    - you can set to vscode by the following setting
        - git config --global core.editor "code --wait"
        - command+shift+P (open command plattee) --> Shell command: Install 'code' command in PATH
        - it could be useful when you want to have detailed commit message description  
- `git commit -m "my commit message"`
    - commit without opening vim or other editor
- `git commit -a -m "my commit message"`
    - one line command to stage+commit
- `git commit --amend`
    - you can use this to amend your **LAST** commit
    - before commit --amend, you can add other files or remove files from staged
    - after commit --amend, it will open the editor for you to amend the commit message (you can just leave it as same)

### Log
- `git log`
- `git log --oneline`
- `git log --graph --oneline`