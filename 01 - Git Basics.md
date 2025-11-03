
## Rename master branch to main

`git branch -m master main`


## Start a git repo


```
git init
git add .
git commit -m "initial commit"
git remote add origin https://github.com/lunarfusion/sajabe.git
git push -u origin main
```

or

```
git push --set-upstream origin main
```


## Gitignore

A file in your local that tells git what not to track. Name the file ".gitignore". List each directory or file on one line.

Example contents:

```
node_modules
/.nova
.DS_Store
package-lock.json
/css
```



## **Remove git**

```
rm -rf .git
```

or

```
sudo rm -rf .git
```



## **Push new branch to remote upstream**

**Upstream (branch already exists in remote)**

```
git push -u upstream branchname
```

## **Push new origin branch to remote**

**Origin (branch exists locally, not yet on remote)**

```
git push -u origin branchname
```


## Create branch

**Create a branch and switch to it**

```
git switch -c my-branch
```

Here is the old way:

```
git checkout -b name_of_branch
```



## Seeing Branches and Commits

**List all branches**

```
git branch -a
```

**Visualize commits**

```
git log --graph
```

or

```
git log --graph --decorate --oneline
```



## Force git to password prompt

https://seankilleen.com/2021/01/how-to-force-git-to-prompt-you-for-a-password/

After git says your login isn't working, do this:

```
git config --system credential.helper
git config --system --unset credential.helper
```

then repeat what you were attempting, in my case it was a push

```
git push
```

enter your git username and an **access token** generated at  
_github > settings > developer settings > access tokens_