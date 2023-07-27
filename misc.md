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
   git ls-tree HEAD <relative path to submodule>
   ```
