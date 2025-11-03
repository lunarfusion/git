
## Rebase branch "experiment" with branch "main"

```
git checkout experiment
git rebase main
```


## Rebase locally and push the rebase to remote

```
git checkout OZA-999--name-of-branch
git rebase main
git push -f
```

**note:** git rebase will result in a commit diff message because the local now has all the commits that the non-rebased remote does not have. This is why we need to force push to rebase (change the history of) the branch.



## interactive rebase

```
git rebase -i main
```


Rebase a spedific # of commits

```
git rebase -i HEAD~29
```