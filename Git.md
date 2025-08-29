# Git Cheatsheet

All the git commands that I find usefull.

## Config

```powershell
git config --global user.name "[user]"
git config --global user.email "[email]"
```

## Commands

- `git init` - starts a git repo in the current working directory.
- `git status` - check the current status of the staged and unstaged files.
- `git add .` - add all unstaged files
- `git add [file|folder]` - stages only the file nor folder.
- `git commit -m [message]` - commit with a message
  - the message should be short with a quick note of what's happening
  - For example: `add: new readme file`
- `git remote add origin [url]` - adds a remote location to push the repo.
- `git push` - pushes all the commits.
- `git push -u origin main` - push all the commits to remote `origin` on the main branch.
- `git reset [commit]` - undo all the commits but changes locally stays.
- `git reset --hard [commit]` - undo all the commits and delete local files.

## Branches

- `git branch [name]` - creates new branch
- `git switch [branch]` - switches to branch
- `git merge [branch]` - merge all the changes from stated branch to current branch.
- `git push --set-upstream origin [branch]` - pushes the branch to the remote.

## Sumbit a PR

Once you submitted the changes to the branch you would be able to create a pull request.

When creating a pull request be sure to add the following:

- Title - what's the pull request fixes or adds.
- Body - explain how you solved the problem if needed.
- Footer - add which issue it solves.
