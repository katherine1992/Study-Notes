# Initial page

**Git** is a **Version Control system** 

**A Version Control System** is a tool that manages changes made to the files and directories

**respository** = files + directories + extra information \(records about the project's history\)

```bash
# To discover which files have been changed since the last save
# To show you which files are in this staging area 
# To show which files have changes that haven't yet been put here 
git status
```

```bash
# To compare the file as it currently is to what you last saved
git diff filename
git diff directory
git diff
```

```bash
git diff data/northern.csv

>>>>
diff --git a/data/northern.csv b/data/northern.csv
# a -> the first version 
# b -> the second version
index e713b17..4c0742a 100644
--- a/report.txt  # lines are removed 
+++ b/report.txt  # lines are added
@@ -1,4 +1,5 @@   
# @@ that tells where the changes are being made.
# (+1,5) -> (start line, number of lines) 
-# Seasonal Dental Surgeries 2017-18
+# Seasonal Dental Surgeries (2017) 2017-18
+# TODO: write new summary
```

### Save changes

```bash
git add # Add one or more files to the staging area
git diff -r HEAD # To see how file differ from the last saved version
                 #  -r  compare to a particular version
                 #  HEAD the most recent commit
git diff -r HEAD path/to/file # view the changes in that file (only that file)
git commit -m "message contents" # save the changes in the staging area
git commit --amend -m "new message" # You can amend it if the previous message was incorrect
```

### text editor - Nano

```bash
nano filename # open a file for editing 
              # or create a new one if it doesn't exist
# ctrl-O write the file out
# ENTER -> confirm the filename
# Ctrl-X -> exit the editor
```

### View a respository's history

```bash
git log # To view the log of the project's history
# space bar -> go down a page
# q -> quit
```

### View a specific file's history

```bash
git log path
```

git does not track files by default, it waits until you have used **git add** at least once before it starts playing attention to a file 

The untracked file won't benefit from version control, so to make sure you don't miss  anything, **git status** will always tell you about files that are in your respository but aren't yet being tracked 

### Ingore files

```bash
# tell Git to ingore certain files (e.g. tempoary/intermediate files during data analysis that you don't want to save)
.gitignore
build * .mpl 
# Git will ignore any file or directory called build, 
# as well as any file whose name ends in .mpl
```

### Remove unwanted files

```text
git clean -n # return a list of files that are in repository
             # but whose history Git is not currently tracking
git clean -f # delete 
```

### Change my Git configuration

```bash
git config --global setting value # change configuration value for all projects on a particular computer
# your name and email are two git settings which should be set on every computer you use
# To record in the log every time you commit a change
# To identify the authors of a project's content to give a credit or assign blame
git config --global user.email ywang257@ncsu.edu
```

### Commit changes selectively

```bash
git add data/northern.csv # only make the stage changes to this file
git commit -m "message"
```

```bash
# Discard the changes that have not yet been staged
git checkout --filename

# Discard the changes that have been staged
git reset HEAD path/to/file # unstage files that you previously staged using "git add"
git checkout -- path/to/file # discard the changes for unstaged file
```

### Restore an old version of a file

```bash
git log -3 report.csv # show you the last three commits invloving report.csv
git checkout 5be6e5 report.csv # replace the current version of report.csv with the version whose hash is 5be6e5
cat report.csv # display the updated contents
git commit -m "message"
```

**branch** allows you to have multiple versions of your work and let you track each version systematically. Each **branch** is like a parallel universe: changes you make in one branch do not affect other branches \(until you merge them back together\)

```bash
git branch # lsit all of branches in a repository
# branch you are currently in will be shown with a * beside its name
```

```bash
git diff branch-1..branch-2 # view the differences between branches
```







