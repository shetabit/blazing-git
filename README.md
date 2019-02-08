# Quick Git Training :bowtie:

### Basics:

- [First-time git setup](#first-time-git-setup)
- [Getting & creating projects (or repositories)](#getting--creating-projects)
- [Snapshotting & working with files](#snapshotting--working-with-files)
- [Branching & merging](#branching--merging)
- [Sharing projects (repositories) through git servers](#sharing-projects-through-git-servers)
- [Inspection & comparison](#inspection--comparison)
- [Using gitignore](#using-gitignore)
- [Undo things](#undo-things)
- [Tips](#tips)
- [ToDo](#todo)
---

### First-time git setup:

If you are new in git (new installer or first-time user) , you need to add some configuration for the first time.

you can *see* or *write* *configs* using `git config` command.

| Command | Description |
| ------- | ----------- |
| `git config --global user.name "your name"` | Add (update) your name into configs. |
| `git config --global user.email yourEmail@example.com` | Add (update) your email into configs. |
| `git config --list` | Show list of current configs. |

---

### Getting & creating projects:

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone <repository-url>` | Create a local copy of a remote repository |

---

### Snapshotting & working with files:

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add <file-name.txt>` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "<commit-message>"` | Commit changes |
| `git commit -am "<commit-message>"` | Add and commit changes in one command |
| `git rm -r <file-name.txt>` | Remove a file (or folder) recursively |
| `git mv <file-name.txt>` `<path/new-file-name.txt>` | Move or rename a file (or folder) |
| `git cp <file-name.txt> <copy-file-name.txt>` | Copy a file (or folder) |

---

### Branching & merging:

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch <branch-name>` | Create a new branch |
| `git branch -d <branch-name>` | Delete a branch |
| `git push origin --delete <branch-name>` | Delete a remote branch |
| `git checkout -b <branch-name>` | Create a new branch and switch to it |
| `git checkout -b <branch-name> origin/<branch-name>` | Clone a remote branch and switch to it |
| `git checkout <branch-name>` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git merge <branch-name>` | Merge a branch into the active branch |
| `git merge <source-branch> <target-branch>` | Merge a branch into a target branch |

---

### Sharing projects through git servers:

> git is a **distributed version control system (DVCS)**, that means you can commit your work locally, and then sync your copy of the repository with the copy on the git server, so your team can have access to the latest files of the project through the git servers.

##### if you want to use remote servers, you have 2 steps:

1. #####  Add your remote server:

| Command | Description |
| ------- | ----------- |
| `git remote add <remote-name> <remote-repository-url>` | Add a remote repository. |
| `git remote set-url <remote-name> <remote-repository-new-url>` | Set a new url for `<remote-name>` repository. (change the given remote's URL) |

2. #####  Push or pull  your files :

| Command | Description |
| ------- | ----------- |
| `git push origin <branch-name>` | Push a branch to your remote repository |
| `git push -u origin <branch-name>` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete <branch-name>` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin <branch-name>` | Pull changes from remote repository |

---

### Inspection & Comparison:

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git diff <source-branch> <target-branch>` | Preview changes before merging |

---

### Using gitignore:

The `.gitignore`file,  tells git which files (or patterns) it *should ignore*. It's usually used to **avoid committing transient files** from your working directory that aren't useful to other collaborators, such as compilation products, temporary files IDEs create, etc.
(Note that all the gitignore files really concern only files that are not already tracked by git)

Create a file and name it  **`.gitignore`**, then use the below rules to ignore files:

- A line starting with `#` serves as a comment.
- An optional prefix `!` which negates the pattern.
- A leading slash matches the beginning of the pathname. For example, `/*.c` matches `cat-file.c` but not `mozilla-sha1/sha1.c`.
- `/**/` matches all sub pathnames, for example, `a/**/b` matches `a/b`, `a/x/b`, `a/x/y/b` and so on.
- A trailing `/**` matches everything inside. For example, `abc/**` matches all files inside directory `abc`, relative to the location of the `.gitignore` file, with infinite depth.
- `[]` matches one character in a selected range, for example [a-z] matches any character from a to z (a,b,c,d to z).
- `?` matches any one character except `/`
- `*` matches anything except `/`

Example:

```git
# this is a comment
# exclude everything except directory foo/bar
/*
!/foo
/foo/*
!/foo/bar
```

---

### Undo things:

We have 2 different states:

- ###### Undoing uncommitted changes
- ###### Undoing committed changes

---

### Tips:

- **Don’t** code for a whole weekend on five different issues and then submit them all as one **massive commit** on Monday. Even if you don’t commit during the weekend, use the staging area on Monday to split your work into **at least one commit per issue**, with a useful message per commit.
- Write your **commit message** in the **imperative**: `Fix bug` and not `Fixed bug` or `Fixes bug`.  This convention matches up with commit messages generated by commands like git merge and git revert.

---

### TODO

we have something to add or complete in future in this document.
you can help us to complete the ToDo list by doing them and creating  **pull request** .

- [ ] Complete the [Undo things](#undo-things) section.
- [ ] Add a section for `Rebasing and cherry-pick` technique.
- [ ] Add a `Tags and versioning` section.
- [ ] Add a some examples in each section.
