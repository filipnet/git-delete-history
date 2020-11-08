# git-delete-history

Delete the complete history of a git repository

## Purpose of use

- Even before you decide to turn a previously private repository into a public one, it may be necessary to remove the commit history first
- The code could have previously contained sensitive data, which was later moved to other files and excluded from the upload with .gitignore

## WARNING

This will remove your history completely, You will not be able to recover it again.

## GIT commands

The following commands can be copy and paste into the command line with line comments, e.g. from VSCode

```
# Create a new orphan branch (will not be shown by command 'git branch')
git checkout --orphan temp_branch
# Add all files to this new orphan branch
git add -A
git commit -am "update"
# Delete main branch
git branch -D main
# Rename the previously created orphan branch to 'main branch'
git branch -m main
# Push new main branch without history data to remote git repository
git push -f origin main
```

## LICENSE

git-delete-history and all individual scripts are under the BSD 3-Clause license unless explicitly noted otherwise. Please refer to the LICENSE
