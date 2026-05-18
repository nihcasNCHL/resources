## What is Git? 
Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.
Git is software for tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development. So Git, is just a software that allows us to manage code changes. It's use-case isn't only for software code though, we can just about use it in any kind of domain like creative art works, document management and versioning and more; that has digital footprint.

## Git architecture overview
Git architecture describes how Git is structured internally and how data flows through the system during version control operations.
Below figure displays the architecture:
![[Pasted image 20260516215143.png|925]]
1. Workspace: This is the project folder where we work on.
2. Staging or Index: The Staging Area is an intermediate layer between your files and commits. It acts like a preparation zone.
3. Local Repository: It is as **Local Repository** where Git repository stored on our own computer.
4. Remote Repository: A version of repository hosted elsewhere. 

## Git terminologies
Git has many important terms that describe how the system works internally and externally.
### 1. Repository (Repo)

A repository is a storage space managed by Git.

It contains:

- project files
- commit history
- branches
- tags
- Git metadata

A Git repository is usually created using:

```bash
git init
```

or downloaded using:

```bash
git clone <url>
```

#### Types of Repository

| Type | Description |
|---|---|
| Local Repository | Stored on your computer |
| Remote Repository | Hosted on server/cloud |

Example remote platforms:

- GitHub
- GitLab
- Bitbucket

---

### 2. Working Directory

The Working Directory is the actual project folder you work in.

Example:

```text
project/
 ├── app.js
 ├── main.py
 └── README.md
```

This is where files are:

- created
- modified
- deleted

---

### 3. Staging Area (Index)

The Staging Area is an intermediate layer between the Working Directory and commits.

Files are added to staging using:

```bash
git add file.txt
```

It allows selective commits.

---

### 4. Commit

A commit is a snapshot of the project at a specific point in time.

Example:

```bash
git commit -m "Added login feature"
```

A commit stores:

- file snapshot
- author information
- timestamp
- commit message
- parent commit reference

---

### 5. Commit Hash

Every commit has a unique identifier called a hash.

Example:

```text
a3f5d21c9b4...
```

Git uses hashes to:

- identify commits
- track history
- ensure integrity

---

### 6. Branch

A branch is an independent line of development.

Default branch names are usually:

- main
- master

Creating a branch:

```bash
git branch feature-login
```

Branches allow safe experimentation.

---

### 7. HEAD

HEAD is a special pointer that refers to the currently checked-out commit or branch.

Example:

```text
HEAD → main
```

Meaning:

- you are currently working on the `main` branch.

---

### 8. Checkout

`checkout` means switching:

- branches
- commits

Example:

```bash
git checkout feature-auth
```

Git updates the Working Directory to match that snapshot.

---

### 9. Clone

`clone` means copying an existing repository.

Example:

```bash
git clone https://example.com/project.git
```

Cloning downloads:

- files
- commits
- branches
- full history

---

### 10. Remote

A remote is a reference to another repository location.

Usually hosted online.

Example:

```bash
git remote -v
```

Common remote name:

```text
origin
```

---

### 11. Origin

`origin` is the default name Git gives to the remote repository during cloning.

Example:

```text
origin → GitHub repository URL
```

---

### 12. Push

`push` uploads local commits to a remote repository.

Example:

```bash
git push origin main
```

---

### 13. Pull

`pull` downloads changes from remote and merges them locally.

Example:

```bash
git pull origin main
```

Internally:

```text
git pull = git fetch + git merge
```

---

### 14. Fetch

`fetch` downloads remote changes without merging them.

Example:

```bash
git fetch
```

Safe way to inspect remote changes first.

---

### 15. Merge

A merge combines changes from different branches.

Example:

```bash
git merge feature-login
```

---

### 16. Merge Conflict

A merge conflict happens when Git cannot automatically decide how to combine changes.

Usually occurs when:

- same file
- same lines
- modified differently

---

### 17. Rebase

`rebase` rewrites commit history by moving commits onto another base.

Example:

```bash
git rebase main
```

Used for cleaner history.

---

### 18. Tag

A tag marks a specific commit.

Often used for releases.

Example:

```bash
git tag v1.0
```

---

### 19. Snapshot

A snapshot is the complete state of the project at commit time.

Git stores projects as snapshots instead of change lists.

---

### 20. Blob

A blob stores file content inside Git.

Blob = Binary Large Object

It stores:

- file data only
- not filename
- not directory structure

---

### 21. Tree

A tree object stores directory structure.

It connects:

- files
- folders
- blobs

---

### 22. Stash

A stash temporarily saves unfinished changes.

Example:

```bash
git stash
```

Useful when switching tasks quickly.

---

### 23. Reflog

`reflog` records movement of HEAD and branch references.

Useful for recovery.

Example:

```bash
git reflog
```

---

### 24. Detached HEAD

Detached HEAD means:

```text
HEAD points directly to a commit
instead of a branch.
```

This happens when checking out old commits directly.

---

### 25. Fork

A fork is a personal copy of someone else's repository on platforms like GitHub.

Common in open-source workflows.

---

### 26. Pull Request (PR)

A Pull Request is a request to merge code changes into another branch.

Usually includes:

- code review
- discussion
- CI checks

---

### 27. Upstream

`upstream` refers to the original repository a fork came from.

Example:

```text
your fork → origin
original repo → upstream
```

---

### 28. Cherry-Pick

`cherry-pick` copies specific commits into another branch.

Example:

```bash
git cherry-pick <commit-hash>
```

---

### 29. Fast-Forward Merge

A merge where Git simply moves the branch pointer forward.

No extra merge commit needed.



## Terms to cover
- tagging
- stashing

