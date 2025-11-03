

## Commit

```
git commit -m “feat: first commit”
```


## Switch commits to a different branch

Uncommit all the local commits to save the changes into a new single commit or new branch.



## Multiline commit messages

`$ git commit index.js -m "My Changes" -m "- Fixed a critical bug"`


## Add another line to a commit message

1. do an interactive rebase
2. reword the commit by replacing "pick" with "reword"
3. add the message to the next line.


## Add files

or changes to the current commit that is not yet pushed

```
git add the_left_out_file
git commit --amend --no-edit
```


## Change the last commit message

```
git commit --amend -m "New message"
git push --force repository-name branch-name
```

or to be safe (incase others have pushed to this branch in the meantime, this will check for that first)

```
git push --force-with-lease repository-name branch-name
```

Amend without changing the commit message

```
git commit --amend --no-edit
```


## Squashing Commits

Combines multiple commits into a single commit.

To squash just the last 3 commits

```
git rebase -i HEAD~3
```

to edit:

```
i
```

add **s** to the beginning of the squashed commit

```
pick 12345eee feat: good commit
s 09876fff throwaway commit
```

when finished:

```
esc
:wq
```

or quit without saving

```
:q!
```

You will probably have to git push **--force**

Prompted to enter commit message,

do :wq again

unless you are also renaming commits (see Renaming Commits notes)

if squashing commits that are not next to one another in order, move them first.  
Commits A, B, and C and you want to merge A and C: Move C under A, then squash.  
idi


## Removing Commits from a Branch

```
git rebase -i HEAD~29
```

```
:%s/pick/d/gc
```

_%multiline, s search, pick, d delete, gc global confirm_

**Enter**

go through multiple commits to drop by hitting y for yes

**y**


## Renaming Commits

```
git rebase -i HEAD~3
```

to edit:

```
i
```

put an **r** next commit to be renamed (do not rename yet)

```
pick 12345eee feat: good commit
r 09876fff commit with dorky name
```

```
esc
:wq
```

In the next screen, rename the commit

```
i
```

rename it

```
esc
:wq
```


## Reordering Commits

```
git rebase -i HEAD~3
```

go to the line you want to move, place the cursor at the start it and do **yy to yank**

```
pick 12345eee feat: good commit 1
pick 98765mmm feat: some other commit
pick 98765ddd feat: another commit
pick 212121xxx feat: good commit 2
```

```
yy
```

go to the start of the line you want that line to follow and do **p to paste**

```
pick 12345eee feat: good commit 1
pick 98765mmm feat: some other commit
pick 98765ddd feat: another commit
pick 212121xxx feat: good commit 2
```

```
p
```

```
pick 12345eee feat: good commit 1
pick 212121xxx feat: good commit 2
pick 98765mmm feat: some other commit
pick 98765ddd feat: another commit
pick 212121xxx feat: good commit 2
```

then highlight the one you just copied and delete it with **dd to delete line**

```
pick 12345eee feat: good commit 1
pick 212121xxx feat: good commit 2
pick 98765mmm feat: some other commit
pick 98765ddd feat: another commit
pick 212121xxx feat: good commit 2
```

```
dd
```