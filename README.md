# git-branch
# Git Branching — Quick Guide

**What is a branch?** A separate copy of your code where you can make changes without affecting the main version.

## Core Commands

| Action | Command |
|---|---|
| List branches | `git branch` |
| Create branch | `git branch name` |
| Switch branch | `git checkout name` |
| Create + switch | `git checkout -b name` |
| Merge branch in | `git merge name` |
| Delete branch | `git branch -d name` |
| Push to GitHub | `git push -u origin name` |
| Cancel a merge | `git merge --abort` |

## Basic Flow

```bash
git checkout -b new-feature   # create + switch
git add .
git commit -m "message"       # save changes
git checkout main             # go back
git merge new-feature         # bring changes in
```

## Conflicts

If both branches change the **same line**, Git stops and asks you to pick a version:

```
<<<<<<< HEAD
your version
=======
their version
>>>>>>> branch-name
```

Edit the file, remove the markers, keep the right text, then:
```bash
git add filename
git commit
```

**Simple analogy:** `main` = finished house, `branch` = a room you're renovating, `merge` = moving that room into the house.
