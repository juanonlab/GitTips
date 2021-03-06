[<< BACK](README.md)

### Workflow: Create a branch and integrate the changes in other

A Common workflow in our everyday life with git. Create a new branch (e.g **development**) from another base branch (e.g **master**) and then integrate the changes to master through a pull request.

- [1/6 Create a branch](#step-16-create-a-branch)
- [2/6 Modify a file and check the status of the branch](#step-26-modify-something-and-then-check-the-status-of-the-branch)
- [3/6 Stage the files](#step-36-stage-the-files)
- [4/6 Status before commit](#step-46-status-before-commit)
- [5/6 Commit changes](#step-56-commit-changes)
- [6/6 Push the changes in a new remote branch](#step-66-push-the-changes-in-a-new-remote-branch)

#### Step 1/6 Create a branch ####

Create the development branch and verify if you are in the good branch (development).

```
git checkout -b development origin/master
```

Verify the current branch.

```
git branch -a
```

Something similar to

```
* development
  master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
```
will be show. 
You are in the development branch. If not: **git checkout development** 

#### Step 2/6 Modify something and then check the status of the branch ####
  
```
git status
```
Something similar to
  
 ```
On branch development
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```
will be show. 
These messages indicate that the branch is updated but you have a file in unstage status. You have to pass the file README.md to the stage status.
  
#### Step 3/6 Stage the files ####
  
```
git add README.md
```
  
If you want to add more files at once, use **git add * **.
  
#### Step 4/6 Status before commit ####
  
```
git status
```
  
Something similar to

```
On branch development
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   README.md
```
will be show. 

#### Step 5/6 Commit changes ####

```
git commit -m "fix comments"
```  
  
#### Step 6/6 Push the changes in a new remote branch ####

A development remote branch will be created.

```
git push -u origin development
```  

Something similar to

``` 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 322 bytes | 322.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/juanon777/GitTips.git
 * [new branch]      development -> development
Branch 'development' set up to track remote branch 'development' from 'origin'.
``` 

will be show.

[<< BACK](README.md)
