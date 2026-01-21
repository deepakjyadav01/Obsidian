#  Core Git Commands (Basic → Intermediate)

**With ONE practical example each**

---

## `git init`

**What it does:**  
Initialises a new Git repository.

**Example:**

`git init`

Creates a `.git/` folder in the current directory.

---

## `git clone`

**What it does:**  
Copies an existing repository locally.

**Example:**

`git clone https://github.com/user/project.git`

 Downloads the project and its history.

---

##  `git status`

**What it does:**  
Shows working tree + staging status.

**Example:**

`git status`

 Tells you which files are modified, staged, or untracked.

---

##  `git add`

**What it does:**  
Stages changes for commit.

**Example:**

`git add index.js`

or

`git add .`

Prepares files for commit.

---

## `git commit`

**What it does:**  
Creates a snapshot of staged changes.

**Example:**

`git commit -m "Add login validation"`

 Saves changes to history.

---

##  `git log`

**What it does:**  
Shows commit history.

**Example:**

`git log --oneline`

 Compact view of commits and hashes.

---

##  `git diff`

**What it does:**  
Shows changes between versions.

**Example:**

`git diff`

 Shows unstaged changes.

---

##  `git branch`

**What it does:**  
Manages branches.

**Example:**

`git branch feature-auth`

 Creates a new branch.

---

##  `git checkout`

**What it does:**  
Switches branches or restores files (older command).

**Example:**

`git checkout main`

 Switches to `main`.

---

## `git switch`

**What it does:**  
Modern branch switching.

**Example:**

`git switch feature-auth`

 Cleaner replacement for checkout.

---

## Detached HEAD

**What it means:**  
HEAD points to a commit, not a branch.

**Example:**

`git checkout a1b2c3d`

 You are now in detached HEAD state.

---

##  `git merge`

**What it does:**  
Combines branches.

### Fast-forward merge example:

`git merge feature-auth`

 Moves branch pointer forward.

### No-fast-forward merge example:

`git merge --no-ff feature-auth`

 Creates a merge commit.

---

##  `git rebase`

**What it does:**  
Rewrites commit base.

### Normal rebase:

`git rebase main`

### Interactive rebase:

`git rebase -i HEAD~3`

 Edit / squash last 3 commits.

---

##  `git reset`

**What it does:**  
Moves HEAD backward.

### Soft:

`git reset --soft HEAD~1`

### Mixed:

`git reset HEAD~1`

### Hard:

`git reset --hard HEAD~1`

⚠️ **Never on shared branches**.

---

##  `git revert` 

**What it does:**  
Safely undoes a commit.

**Example:**

`git revert a1b2c3d`

 Creates a new commit that reverses changes.

---

## ⭐ Interview gold line (memorise)

> **“Reset rewrites history, revert preserves history by creating a new commit.”**
