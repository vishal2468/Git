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
