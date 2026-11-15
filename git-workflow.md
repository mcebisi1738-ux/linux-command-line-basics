# My Git Workflow

This guide records the Git workflow I am practising in DevOps Project 2.

## Local workflow

1. Edit or create a project file.
2. Run `git status` to inspect changes.
3. Run `git add <filename>` to stage a specific file.
4. Run `git diff --staged` to review the staged changes.
5. Run `git commit -m "Describe the change"` to save a checkpoint.

## Sharing changes

- `git push` uploads local commits to GitHub.
- `git pull` fetches and integrates changes from the remote branch.

## Useful checks

- `git log --oneline` shows a compact commit history.
- `git diff` shows unstaged changes to tracked files.
- A clean working tree means there are no uncommitted changes.
