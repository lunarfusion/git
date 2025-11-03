
Careful with stashing, as it can be very difficult to recover lost work if you have a lot of stashes.


## Stash local changes and pull

```
git add *
git stash
git pull
```


**Stash Local Work (no need to add modified files)**

```
git stash
```


**Apply (bring back) your most recent stash and remove it**

```
git stash pop
```

`git stash pop` **_throws away_** _the last stash after applying it._


**Apply (bring back) your most recent stash and don't remove it**

```
git stash apply
```

`_git stash apply_` **_leaves the stash it in the stash list_** _for possible later reuse (or you can then_ `git stash drop` _it to remove it from the list)._


**List all stashes**

```
git stash list
```


**Apply a different stash from the list (change the number)**

```
git stash apply stash@{2}
```


## Branch from Stash

**Create a new branch from the same commit you were on when you stashed the changes, and applies the stashed changes to that new branch.**

```
git stash branch
```


## Name your stashes

```
git stash push -m "my_stash_name"
```

To _apply_ a stash by name:

```
git stash apply stash^{/my_stash_name}
```

To _apply and remove_ a stash by name:

```
git stash pop stash^{/my_stash_name}
```


## Delete all stashes

The following command deletes all your stashes:

```
git stash clear
```


## Use Stashing to remove untracked files from the branch (unconventional local reset method)

```
git add --all
git stash
git stash dropp
```