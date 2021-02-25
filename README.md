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

