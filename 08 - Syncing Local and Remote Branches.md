
## To update a local copy of a branch to work on it:

```
git fetch upstream branchname
git pull
```


## Fetch all remote branches & update local branches

```
git fetch --all
git pull --all
```


## Connecting local branches to remote branches

Create remote branch corresponding to local branch and push from local to remote

```
git push --set-upstream origin XXX-999--name-of-branch
```


## Connect local branch to remote counterpart that already exists

```
git checkout master
git branch --set-upstream-to=origin/main main
git checkout dev
git branch --set-upstream-to=origin/dev dev
```


## Sync local main o remote main

```
git fetch --all
git branch --set-upstream-to=upstream/main main
```

```
git branch --set-upstream-to=master/main main
```


## Adding Upstream

**Add upstream**

```
git remote add upstream http://github.upstream-repo-url
```


**Add upstream and fetch it at the same time**

```
git remote add -f upstream http://github.upstream-repo-url
```


**Verify upstream**

```
git remote -v
```


## Remove Upstream

```
git remote rm upstream
```