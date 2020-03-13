# Git and GitHub Cheat Sheet



## Remove sensitive data from repository and repository history

Taken from this GitHub [webpage](https://help.github.com/en/github/authenticating-to-github/removing-sensitive-data-from-a-repository)

'''
git filter-branch --force --index-filter \
  "git rm --cached --ignore-unmatch data_clean/GP010016_fast.csv" \
  --prune-empty --tag-name-filter cat -- --all
'''

## Tagging

Taking from the git book [website](https://git-scm.com/book/en/v2/Git-Basics-Tagging)

Create a tag

`git tag -a v1.4 -m "my version 1.4"`

Seeing all tags

`git tag`

See tag data

`git show v1.4`

Push git tags to remotes

`git push origin v1.4`

Deleting tags

`git tag -d v1.4` and then `git push origin --delete v1.4`

## Ammend last commit

`git commit -amend --no-edit`

Undo the last commit amend

`git reset --soft -HEAD@{1}`

Amend commit message

`git commit --amend` or `git commit --amend -m "New commit message"`

