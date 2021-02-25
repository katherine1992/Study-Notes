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



