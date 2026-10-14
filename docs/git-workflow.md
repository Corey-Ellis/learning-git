# Git Branching and Pull Request Workflow

## Objective
To understand what "Markdown" is, and how to use it.

| Command | Purpose |
|---|---|
| `git status` | Shows the current branch and working tree status | 
| `git branch` | Lists local branches |

When Git displays "nothing to commit, working tree clean," it means there are no outstanding file changes to commit. The files in my working directory match my latest local commit.

### 2. Create a Feature Branch

| Command | Purpose |
|---|---|
| `git switch -c add-markdown-documentation` | Creates a new branch and switches to it |
| `git branch` | Lists local branches and identifies the active branch |

A feature branch allows me to make changes without directly
affecting the main branch. In a real working project, this
helps protect the stable version while I experiment with
new features or configurations.

Once I have tested and verified my changes, I can merge
the feature branch into main.

### 3. Modify Project Files

I opened my repository in VS Code and created a new
Markdown file named `git-workflow.md` inside the `docs`
folder.

I used Markdown syntax to organize my documentation
with headings, tables, and command explanations.

Pressing `Ctrl + S` saved my changes locally, but did
not create a Git commit or upload anything to GitHub.

### 4. Stage and Commit Changes

| Command | Purpose |
|---|---|
| `git status` | Checks for modified, staged, or untracked files |
| `git add docs/git-workflow.md` | Stages the file for the next commit |
| `git commit -m "Document Git branching workflow"` | Records the staged changes in local Git history |

An untracked file is a new file that Git has not started tracking. Using `git add` stages the file so it can be included in the next commit.

A commit records a snapshot of the staged changes in the local repository.

### 5. Push the Branch

| Command | Purpose |
|---|---|
| `git push -u origin add-markdown-documentation` | Uploads the local branch and its commits to GitHub and sets its upstream |

A local repository is stored on my computer, while a remote repository is hosted on GitHub.

After committing my changes locally, I used `git push` to upload them to GitHub.

Pushing a feature branch does not automatically merge its changes into the main branch.

### 6. Open and Review a Pull Request

After pushing my feature branch to GitHub, I created a pull request to propose merging my changes into main.

I reviewed the changes using the "Files changed" tab to verify that the documentation was accurate and formatted correctly.

A pull request allows changes to be reviewed before they are merged into another branch.

### 7. Merge and Synchronize Main

| Command | Purpose |
|---|---|
| `git switch main` | Switches to the local main branch |
| `git pull origin main` | Downloads and integrates changes from GitHub's main branch |
| `git status` | Verifies the current branch and working tree status |
| `git branch -d add-markdown-documentation` | Deletes the local feature branch after merging |

After reviewing my pull request on GitHub, I merged the feature branch into main.

However, merging on GitHub did not automatically update the files on my computer.

I used `git switch main` to return to my local main branch, followed by `git pull origin main` to synchronize it with GitHub.

Finally, I verified the repository status.

## Verification

I verified that my pull request was successfully merged by checking its status on GitHub and confirming that `docs/git-workflow.md` appeared in the main branch.

I then used `git pull origin main` to synchronize my local repository with GitHub.

Finally, I ran `git status` to confirm that my local main branch was up to date and my working tree was clean.