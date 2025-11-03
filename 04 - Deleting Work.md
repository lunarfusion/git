
## Restore / Checkout

```
git restore filedir/filename
```


## **Delete Branches**

**Delete a local branch**

```
git branch -d the_local_branch
```

**Delete remote branch**

```
git push origin :the_remote_branch
```

## Delete ALL work and start over

**To remove all local changes and start over from remote branch (you will lose your work!)**

```
git fetch
git reset --hard origin/<branch>
```

## Delete untracked files and start over

Remove all untracked files, The simple way is to **add all of them first** and **reset the repo** as below

```
git add --all
git reset --hard HEAD
```


## Remove the last commit you pushed

_only on non-main branches_  

**1.**  
**View your local commit history:**

```
git log
```

**2. revert commit method 1:**  
copy the last good SHA that you want to revert to

```
git reset --hard sha#goeshere
```

**2. revert commit method 2:**

```
git reset --hard HEAD~1
```

**3. push the change**

```
git push -f
```

❗**==Do not push -f from MAIN==**


## Discard all local changes to all files permanently

```
git reset --hard
```


## **Discard local changes to a specific file**

```
git reset --hard
git checkout main--filenameter --filename
```

_(no spaces in double dash)_