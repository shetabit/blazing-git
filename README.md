# Quick Git Training

### Basics:
- First-time git setup
- Getting & creating projects (or repositories)
- Snapshotting and working with files
- Branching & merging
- Sharing projects (repositories) through git servers
- Inspection & comparison

---

### First-time git setup :

If you are new in git (new installer or first-time user) , you need to add some configuration for the first time.

you can *see* or *write* *configs* using `git config` command.

| Command | Description |
| ------- | ----------- |
| `git config --global user.name "your name"` | Add (update) your name into configs. |
| `git config --global user.email yourEmail@example.com` | Add (update) your email into configs. |
| `git config --list` | Show a list of current configs. |

---

### Getting & creating projects:

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone <repository-url>` | Create a local copy of a remote repository |

---

### Snapshotting and working with files:

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add <file-name.txt>` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "<commit message>"` | Commit changes |
| `git commit -am "<commit message>"` | Add and commit changes in one command |
| `git rm -r <file-name.txt>` | Remove a file (or folder) recursively |
| `git mv <file-name.txt>` `<path/new-file-name.txt>` | Move or rename a file (or folder) |
| `git cp <file-name.txt> <copy-file-name.txt>` | Copy a file (or folder) |

---

### Branching and merging:

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

if you want to use remote servers, you have 2 steps:

1. #####  Add your remote server

| Command | Description |
| ------- | ----------- |
| `git remote add <remote-name> <remote-repository-url>` | Add a remote repository. |
| `git remote set-url <remote-name> <remote-repository-new-url>` | Set a new url for `<remote-name>` repository. |

2. #####  Push your files into the remote server:

| Command | Description |
| ------- | ----------- |
| `git push origin <branch name>` | Push a branch to your remote repository |
| `git push -u origin <branch name>` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete <branch name>` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin <branch name>` | Pull changes from remote repository |

---

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git diff [source branch] [target branch}` | Preview changes before merging |

---

