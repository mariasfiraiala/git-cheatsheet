# Misc `git` Commands

* **Show all files from a commit**

   ```console
   $ git diff-tree --no-commit-id --name-only <commit hash> -r
   ```

* **Diff for a file between 2 branches**

   ```console
   $ git diff <branch1> <branch2> -- <relative path to file>
   ```

* **Create upstream**

   ```console
   $ git remote add upstream <url>
   ```

* **Create tracking branch**

   ```console
   $ git checkout --track <remote branch name>
   ```

* **Rebase with remote**

   ```console
   $ git pull --rebase <remote> <branch>
   ```

* **Blame for individual lines**

   ```console
   $ git blame -L <start-line>,<end-line> <file-name>
   ```

* **Copy file from one branch to another**

   ```console
   $ git checkout <source branch> <file>
   ```

* **Get the current commit id of a submodule**

   ```console
   $ git ls-tree HEAD <relative path to submodule>
   ```

* **Reset branch with changes from another branch**

   ```console
   $ git checkout <branch to be reset>
   $ git reset --hard <branch to reset with>
   ```

* **Remove file from last commit without deleting it**

   ```console
   $ git reset --soft HEAD~1
   $ git restore --staged <file to remove>
   $ git commit -c ORIG_HEAD
   ```

* **Entirely remove file from git history**

   ```console
   $ git filter-branch --index-filter \
  'git rm --ignore-unmatch --cached <file to remove>' -- <commit to start removing from>^..
   ```

* **Remove files from remote without deleting them from local using gitignore**

   ```console
   $ git rm --cached $(git ls-files -i -c -X .gitignore)
   ```

* **Stash only a portion of a file**

   ```console
   $ git stash --patch <file>
   ```

* **Squash last n commits into one**

   ```console
   $ git reset --hard HEAD~<n commits>
   $ git merge --squash HEAD@{1}
   $ git commit
   ```
