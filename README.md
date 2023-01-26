# Git Basics
## Java brains Git Basic notes

## status 
git status 

## stage 
git add <filename>

## commit 
git commit -m "message"

## three state architecture 
* working directory 
* staging area
* commit state

## can add multiple files at once 
git add <filename1> <filename2> ..

## even if multiple files are changed we are allowed to add only a few of them.
git add <filename1>

## we are not staging files but changes
modify a file 
    -> git add <file> 
    -> modify the same file again 
    -> git status 
    -> we will see file as both "changes to be commited" and "changes not staged"  
    -> this implies that changes is what is staged 
    -> git add <file> 
    -> git commit 
    -> this will merge the changes and commit the changes
