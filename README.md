# Git-branching-
This documentation contains the concepts of Learn Git Branching.

#Learn Git Branching
Learn Git Branching is an interactive, browser-based learning platform that helps users understand how Git works internally through real-time visual diagrams, covering concepts such as commits, branches, HEAD, merging, and rebasing.

# Level-1 [Introduction Sequence]
1.Introduction to Git Commits
What is Git Commit?
A Git commit is a record that saves the current state of a project in a Git repository. It stores the changes made to files along with a message describing those changes, allowing Git to track the project’s history over time.
<img width="1600" height="731" alt="image" src="https://github.com/user-attachments/assets/6c07cfac-a61b-48a7-bcfb-4f7f88f7a42c" />
# COmmands Executed
```bash
git commit
```
```
git commit
```
This screenshot shows how commits are created in Git.

Each circle (C0, C1, C2, C3) represents a commit made one after another.
The (main*) label shows the current branch, and it points to the latest commit (C3).
Every time git commit is used, a new commit is added and the main branch moves forward.
This helps us understand how Git keeps track of changes.

# 2.Introduction to Git Branching
What is Git Branch?
A branch in Git is like a separate workspace for your code. It allows you to work on new features or fixes without affecting the main code

What is Git Chechout?
The git checkout command is used to switch between these branches, so your files and code update to match the branch you select.
<img width="1600" height="732" alt="image" src="https://github.com/user-attachments/assets/efce2922-f581-4f8e-86c4-39a19c45248f" />

# Commands Executed
```bash
git branch bugfix
```
```
git checkout bugfix
```
This screenshot shows how to create and switch to a new branch in Git using Learn Git Branching.
The commits C0 and C1 are displayed, with C1 being the latest commit.

A new branch named bugfix has been created from commit C1 using git branch bugfix, and it has been checked out using git checkout bugfix.
The * symbol next to bugfix indicates that HEAD is currently on this branch.
The main branch still points to commit C1, but the active branch is now bugfix.

# 3.Introduction to Git Merging

What is Git Merging?
Git merging is the act of combining changes from one branch into another branch so that both branches work exists together in a single branch.
<img width="1600" height="723" alt="image" src="https://github.com/user-attachments/assets/d20565df-7bf8-45e8-bd1b-6bd175311ea8" />
# COmmands Executed
```bash
git branch bugfix
```
```
git checkout bugfix
```
```
git commit
```
```
git checkout main
```
```
git commit
```
```
git merge bugfix
```
This screenshot illustrates the Merging in Git level from Learn Git Branching, showing how Git manages multiple branches and combines them.
The circles labeled C0, C1, C2, C3, and C4 represent individual commits, with the history first moving linearly from C0 to C1 and then splitting into two paths.
From commit C1, a new branch named bugfix is created and points to commit C2, while the main branch continues independently with commits C3 and C4.
The label main* indicates that the main branch is currently checked out, with the * symbol showing that HEAD is pointing to main at commit C4.
The curved lines in the diagram visually represent the divergence of the two branches and their integration through a merge.

#4.Introduction to Rebase
What is Git Rebase
Git rebase is the process of moving or replaying commits from one branch onto another branch, changing the base commit so the history becomes linear.



