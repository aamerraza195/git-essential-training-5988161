# Welcome to Git Learning!

This repository is designed to help you learn and practice Git. Explore the examples, follow the guides, and experiment with version control to improve your skills.

//git commands

1. `git init` – Initialize a new Git repository.
2. `git clone` – Copy a remote repository to your local machine.
3. `git status` – Show the current state of the working directory and staging area.
4. `git add` – Stage changes for the next commit.
5. `git commit` – Save staged changes to the repository.
6. `git log` – View the commit history.
7. `git diff` – Show changes between commits, branches, or files.
8. `git branch` – List, create, or delete branches.
9. `git checkout` – Switch branches or restore files.
10. `git push` – Upload local commits to a remote
11. `git remote add origin <url>` – This command adds a remote repository and names it "origin". The `<url>` is the address of the remote repository (usually on GitHub, GitLab, etc.). After adding, you can use "origin" as a shortcut to interact with the remote repository, such as pushing or pulling

**Difference between `git remote add origin` and `git clone`:**

- `git clone <url>` copies an entire remote repository to your local machine and automatically sets up the remote called "origin".

- `git remote add origin <url>` is used after you have already created a local repository (with `git init git add . git commit -m`) and want to connect it to a remote repository. It does not copy any files; it just links your local repo to the remote.

  //your local repository folder can have any name, and you can connect it to a remote repository with a different name. The connection is managed by the remote URL, not the folder name. The remote is usually named "origin" by convention, but you can use any name when adding

first you have to do git pull so synchronized any new files in remote repo that are not locally available and resolve any conflicts then do git push

first pull will give error if there are already files in the remote repo so use because your local branch (e.g., `main`) is not yet set to track a remote branch (e.g., `origin/main`).  
To fix this, you should set the upstream branch so Git knows which remote branch to pull from and push to.
git branch --set-upstream-to=origin/main main

**refusing to merge unrelated histories**
This error occurs when you try to merge or pull from a remote repository that has a different commit history than your local repository (for example, both have initial commits that are not related).
**To resolve this, use:**
git pull origin main --allow-unrelated-histories

first git push will give folloeing error fatal: The current branch main has no upstream branch.To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

//When you create a new branch (like `main`) locally and try to push it to a remote for the first time, Git tells you there is no "upstream" branch (a remote branch to track).This command pushes your local `main` branch to the remote named `origin` and sets it to track the remote branch, so future pushes and pulls will work

//Yes, you will still get this error on the first push from your local `main` branch if it is not yet linked (tracking) the remote `main` branch, even if the remote already has a `main` branch.  
You need to use `git push --set-upstream origin main` to establish the tracking relationship between your local and remote branches. After this, future pushes and pulls


12. `git fetch` – Download new data from a remote repository without merging it into your local branch.
13. `git merge <branch>` – Combine changes from another branch into your current branch.
14. `git reset` – Undo changes by resetting your current HEAD to a specified state.
15. `git rm <file>` – Remove files from your working directory and staging area.
16. `git stash` – Temporarily save changes that are not ready to commit.
17. `git tag <name>` – Mark specific points in history as important (like releases).
18. `git show <commit>` – Display information about a specific commit.
19. `git remote -v` – List all remotes and their URLs.
20. `git config` – Set configuration options for Git (like username and email).
21. `git reflog` – Show a log of where your HEAD and branch
22. `git mv <old> <new>` – Rename or move a file in your repository.
23. `git cherry-pick <commit>` – Apply the changes from a specific commit to your current branch.
24. `git blame <file>` – Show who last modified each line of a file.
25. `git clean -f` – Remove untracked files from your working directory.
26. `git archive` – Create an archive (zip/tar) of files from a repository.
27. `git shortlog` – Summarize `git log` output by author.
28. `git describe` – Show a human-readable name for a commit based on tags.
29. `git bisect` – Find the commit that introduced a bug using binary search.
30. `git submodule` – Manage repositories embedded within your main repository.
31. `git revert <commit>` – Create a new commit that undoes the changes from a previous
32. `git log --oneline` – Show the commit history in a simplified, one-line-per-commit format. Useful for quickly viewing commit