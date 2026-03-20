
## Update main branch, then create a new branch and push it to remote

```
git checkout main
git pull --rebase
git checkout -b new-branch-name
git push -u origin new-branch-name 
```


## Switch to remote branch

```
git switch <branchname>
```


## Delete a local branch

```
$ git branch -D <local-branch>
```

Do this after the work has been merged.

## Git Switch

```
git switch my-branch              # same as git checkout my-branch
git switch -c my-branch           # same as git checkout -b my-branch
git switch -c my-branch HEAD~3    # branch off HEAD~3
git switch --detach HEAD~3        # checkout commit without branching
```


## What branches exist?

```
git branch -a 
```


## Get all remote branches

```
git fetch --all
git pull --all
```