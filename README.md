# Git Basics

## Java brains Git Basic notes

## see current status 
```
git status
```

## stage your changes
```git:
git add <filename>
```

## commit your changes
```
git commit -m "message"
```

## Three state architecture 

* working directory 
* staging area
* commit state

## can add multiple files at once 
```
git add <filename1> <filename2> ..
```

## add only a few changes(files)
```
git add <filename1>
```

## We are not staging files but changes
    ->modify a file 
    -> git add <file> 
    -> modify the same file again 
    -> git status 
    -> we will see file as both "changes to be commited" and "changes not staged"  
    -> this implies that changes is what is staged 
    -> git add <file> 
    -> git commit 
    -> this will merge the changes and commit the changes

## Type long commit message
```
git commit
```

## See previous commits
```
git log
```

## See changes in commits
```
git log -p
```

## Remove changes to files before staging 
```
git checkout -- <file1>
git checkout -- <file1> <file2>
git checkout .
```

## Unstage changes after staging 
* Restore specified paths in the working tree with some contents from a restore source
* restore can do all that checkout can do and more
```
git restore --staged <file>
```

## remove unsatged changes using restore
```
git restore <file>..
```

## amend the previous commit 
-> add new changes to staging area
-> git commit --amend
-> this opens editor and we can even change our commit message
```
git commit --amend
```

## amend just the message
-> use git commit --amend without adding anything in satging area

## show the unstaged changes 
```
git diff
```

## show the staged changes 
```
git diff --staged
```

## prevent a file/folder to be added to repo
* Add the file/folder in .gitignore file
* If some file if already in the commits , we cannot simply ignore that file
* it supports glob format("global pattern match")

## commits
* see commits.png
* creates something like blockchain.
* there is id for commit , check sum , hash , and pointer to pvs block.

## branching 
* see pranch.png
* we may want to work on multiple issues on a same project in that case branching comes handy.

## lists all the branches in the repo
* current branch name is in green and has "*" before its name.
```
git branch
```

## create a new branch 
```
git branch <branch-name>
```

* git keeps track of current branch using head pointer.
* head is a pointer that points to current branch all the time.

## switch between branch 
```
git checkout <branch-name>
```
* we can commit to the new branch. and the state of the pointers will change.


## create a new branch and checkout to it at once
```
git checkout -b <new-branch-name>
```

## commit and add at the same time 
```
git commit -a -m "message"
```

## merge a branch that is behind
* this is just changing the pointers
* fast forward strategy is used.
* the branch that is behind just "fast forwards" the pointer to the ahead branch
```
git merge <branch-that-is-ahead>
```

## merge two diverged branches
* this will create a auto commit for merge request and will merge the 2 branches with net total changes.
* "recursive" strategy is used.
```
git merge <branch-that-has-diverged>
```

## important points 
* head points to pointers of the branches.
* every commit points to pvs commits 
* merge commits points to 2 pve commits

## graphical view of the branches
```
git log --graph
```

## delete branches
```
git branch -d <branch-name>
```
* cannot delete the current branch.
* this is just deleting the pointers.
* deleting stream of work is a big deal.

## go back to a previous commit 
```
git checkout <branch-hashcode>
```
this is move the head pointer to the respective commit.
this state is called detached head state

## give name to a detached head state
```
git branch <detached-head-branch-name>
```