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
<img width="1600" height="735" alt="image" src="https://github.com/user-attachments/assets/b4680746-9885-4de7-9c8b-366f73048951" />
# Commands Executed
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
git checkout bugfix
```
```
git rebase main
```
This screenshot shows how rebasing works in Git using two branches.
The circles (C0, C1, C2, C3) represent commits created at different times on different branches.
The main branch has its own commits, and the bugFix* label shows the branch where the bug fix work is done.
First, commits are made separately on the main and bugFix branches.
When the command git rebase main is used on the bugFix branch, Git takes the bug fix commit and places it on top of the latest commit of the main branch.
After rebasing, both branches contain the same changes, and the commit history becomes clean and straight.
This helps us understand how Git can organize commits neatly while keeping all changes.
The commit history begins linearly from C0 to C1, after which it splits into two branches.
The main branch points to commit C3, while the bugfix* branch is currently checked out and points to C2, as indicated by the * symbol showing that HEAD is on the bugfix branch.
The diagram shows that the bugfix commit has been moved and reapplied on top of the latest commit of the main branch, resulting in a straight, linear history.
The renaming of the commit to C2′ visually represents that the commit was recreated during the rebase process.

# Level-2 [Ramping Up]
1.Detach yo' HEAD

Detach yo’ HEAD means that you are no longer working on a branch.
Normally, HEAD points to a branch like main or bugFix. In a detached HEAD state, HEAD points directly to a commit instead of a branch.
This usually happens when you checkout a specific commit.
In this state, you can look at old code or test something, but any new commit you make will not belong to a branch.
If you switch to another branch, those commits can be lost unless you create a new branch.
This helps us understand why staying on a branch is important when making changes.





