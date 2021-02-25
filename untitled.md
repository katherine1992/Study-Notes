# page 2

### create a branch & switch to that branch

```bash
git checkout branch_name # switch to that branch
git checkout -b branch_name # create and switch to that branch
```

### merge two branch

```bash
git merge summary-statistics master # merge one branch (source = summary-statistics) into another (destination = master)
```

### Conflict

```bash
# there is a conflict during the merge
git status # tell you which files have conflicts that you need to solve
```

### create a brand new repository

```bash
git init optical
```

### Turn an existing project into a Git repository

```bash
pwd # current directory dental, which is not yet a Git repository
git init # Initiate a folder into a Git repository
```

### Create a copy of an existing repository - clone

```bash
git clone URL # URL identifies the reposiroty you want to clone
git clone /exisiting/project newprojectname
```

### Find out where a cloned repository originated

```bash
git remote # Git remember where the origial reposistory was
# it does this by storing a remote om the new repository's configuration
git remote -v # v for verbose which shows remote's URLs
```

### Define remotes

```bash
git remote add remote-name URL # add more remotes
git remote rm remote-name
```

**remote respository** is often a repository in an online hosting service like Github. A typical workflow is that you pull in your collaborator's work from the remote repository so you have the latest version of everything, do some work yourself, then push your work back to the remote so that your collaborators have access to it

```bash
git pull remote branch # get everything in branch in the remote repository indentified by remote
                       # and merge it into the current branch of your local repository
cd dental  # you are in the master branch of the repository dental
git pull origin master 
# pull all changes from the master branch of the remote repository called origin
# origin -> remote repository name 
# master -> branch you want to pull in                
```

### want to pull when I have unsaved changes

remember you should have committed all your local changes if you want your git pill to turn smoothly 

```bash
git pull origin master
# failed due to the unsaved work in your local repository
git checkout report.txt # discard the changes in you dental reposistoru

```

### push my changes to a remote repository

push the changes you have made locally into a remote repository

```bash
git push remote-name branch-name 
# push the contents of your branch (branch-name) into a branch with the same name
# in the remote repository associated with (remote-name)
```

## What happens if my push conflicts with someone else's work?

```bash
git origin master 
# Git refused to excute your push to prevent you overwriting remote work
git pull origin master # bring your repository up to date with origin
# it will open up an editor that you can exit with Ctrl+X

```

