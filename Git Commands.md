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
- `git remote add origin <url>` is used after you have already created a local repository (with `git init`) and want to connect it to a remote repository. It does not copy any files; it just links your local repo to the remote.

Yes, your local repository folder can have any name, and you can connect it to a remote repository with a different name. The connection is managed by the remote URL, not the folder name. The remote is usually named "origin" by convention, but you can use any name when adding
