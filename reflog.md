### Reflog (Reference Logs)
- Git keeps a record when you do git instructions. We can view and update these reference logs using the git reflog command.
- `git reflog`
    - reflog command accepts subcommand `show`, `expire`, `delete`, `exists`. Show is the only commonly used variant, and it's the default subcommand.
- `git reflog show HEAD`
    - show the log of a specific reference (default to HEAD)
    - for example, to view the logs for the tip of the main branch, we could run `git reflog show main`


### Reflog References
- `name@{qualifier}`
- We can use this syntax to access specific ref pointers and can pass them to other commands including `checkout`, `reset`, `merge`, `diff`...
- **Timed References**
    - Every entry in the reference logs have a timestamp associated with it. We can filter reflogs entries by time/date by using time qualifiers like:
        - `git reflog master@{one.week.ago}`
        - `git checkout bugfix@{2.days.ago}`
        - `git diff main@{0} main@{yesterday}`
    - We can sometimes use reflog entries to access commits that seem lost and are not appearing in git log.



### Limitations!
- Git only keep reflogs on your local activity. They are not shared with collaborators.
- Reflogs also expire. Git cleans out old entries after around 90 days, though it can be configured.