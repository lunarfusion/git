
Commands I tend to use frequently.

___________
## Branching

**Create branch**

```
git switch -c my-branch
```


**List all branches**

```
git branch -a
```


**Update main branch, Create a new branch and push it to remote**

```
git checkout main
git pull --rebase
git switch -c my-branch
git push -u origin new-branch-name
```

## Commits

**Conventional Commit Templates**

```
git commit -m “feat: I made a thing”
```

```
git commit -m “feat!: I made a thing that could break things”
```

```
git commit -m “chore: routine cleaning”
```

```
git commit -m “fix: I fixed a broken thing"
```


**Add files to your commit**
(or add changes to the current commit that is not yet been pushed)

```
git add the_left_out_file
git commit --amend --no-edit
```


## Push new branch to remote

```
git push -u upstream branchname
```


## Update a local copy of a branch to work on it

```
git fetch upstream branchname
git pull
```

## Rebase

**Rebase branch "experiment" with branch "main"**

```
git checkout experiment
git rebase main
```


**Rebase locally and push the rebase to remote**

```
git checkout OZA-999--name-of-branch
git rebase main
git push -f
```


**Rebase - interactive**

```
git rebase -i main
```


**Rebase a specific # of commits**

```
git rebase -i HEAD~29
```


## Add upstream repo

```
git remote add upstream http://github.upstream-repo-url
```

