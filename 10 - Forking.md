## Syncing a fork to main

**Clone fork**

```
git clone [git@github.com](mailto:git@github.com):YOUR-USERNAME/YOUR-FORKED-REPO.git
```


**Add upstream**

```
cd into/cloned/fork-repo

git remote add upstream git://[github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM.git](http://github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM.git)

git fetch upstream
```


**Checkout main

```
git checkout main
```


**Pull Upstream**

```
git pull upstream master
```


**Merge main with upstream**

```
git merge upstream/main
```


**Update fork in github**

```
git push
```