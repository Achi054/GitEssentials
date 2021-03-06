# **Git Commands**
# Table of contents
1. [Introduction](#introduction)
2. [Project Creation](#project-creation)
3. [Repo initialization](#initialization)
4. [Link to remote](#remote)
5. [Add file to git](#add)
6. [Commit your changes](#commit)
7. [Create new local branch](#checkout)
8. [Push local changes to server](#push)
9. [Delete local branch](#delete)
10. [Merge change from another branch](#merge)
11. [Rebase change from another branch](#rebase)
12. [Revert your commits](#revert)
13. [Squash all commits](#squash)

<a name="introduction"></a>
## _Introduction_
**Git** is a distributed version control tool that can manage a development project's source code and its history.

**GitHub** GitHub is a cloud based platform built around the Git tool.

The key difference between **Git** and **GitHub** is that **Git** is an open-source tool developers install locally to manage source code, while **GitHub** is an online service to which developers who use Git can connect and upload or download resources.

<a name="project-creation"></a>
## _Project creation_
Create a folder in your file system. Navigate within it to have it as local repo for your source code.

<a name="initialization"></a>
## _Repo initialization_
_git init_ is one way to start a new project with Git. To initialize a repository, Git creates a hidden directory called _.git_. That directory stores all of the objects and refs that Git uses and creates as a part of your project's history. This hidden _.git_ directory is what separates a regular directory from a Git repository.
```text
git init
```

<a name="clone"></a>
## _Clone your remote repository_
The _git clone_ command is used to create a copy of a specific repository or branch within a repository.
```text
git clone <repo-url>
```

<a name="remote"></a>
## _Link to remote_
The _git remote_ manages the set of remotes that you are tracking with your local repository.
```text
git remote add origin <repo-url>
```

<a name="add"></a>
## _Add file to git_
The _git add_ command adds new or changed files in your working directory to the Git staging area.
```text
git add <file-name>
```

<a name="commit"></a>
## _Commit your changes_
Commits are the building blocks of "save points" within Git's version control.
```text
git commit -m "<commit-message>"

Flavors:
To add all files and commit
git commit -am "<commit-message>"
```

<a name="checkout"></a>
## _Create new local branch_
The _git checkout_ command lets you navigate between the branches created by git branch. The _git checkout_ command accepts a _-b_ argument that acts as a convenience method which will create the new branch and immediately switch to it.ranch.
```text
git checkout <branch-name>
git switch <branch-name>

Flavors:
To create new branch
git checkout -b <branch-name>
git switch -c <branch-name>
```

<a name="push"></a>
## _Push local changes to server_
The _git push_ uploads all local branch commits to the corresponding remote branch.
```text
git push origin <branch-name>
```

<a name="delete"></a>
## _Delete local branch_
The _git branch -d or -D_ delete a local branch in Git.
Make sure to be on another branch than the branch to delete.
```text
Flavors:
To delete local branch, if no unmerged changes
git branch -d <branch-name>

To delete local branch, if force deletion
git branch -D <branch-name>

To delete branch at remote
git push -d origin <branch-name>
```

<a name="merge"></a>
## _Merge change from another branch_
The _git merge_ will combine multiple sequences of commits into one unified history. In the most frequent use cases, git merge is used to combine two branches.
Make sure to be on the target branch.
```text
git merge <source-branch-name>
```

<a name="rebase"></a>
## _Rebase change from another branch_
The _git rebase_ is used for moving or combining a sequence of commits to a new base commit.
Make sure to be on the target branch.
```text
git rebase <source-branch-name>
```

<a name="revert"></a>
## _Revert your commits_
The _git revert_ command is used for undoing changes to a repository's commit history.
```text
Flavors:
git revert --hard HEAD~1
--hard: Reverts without trace.

git revert --soft HEAD~1
--soft: Reverts to previous commit with original commit changes merged.

HEAD~(n): _n_ signifies number of commit to revert.
```

<a name="squash"></a>
## _Squash all commits_
The _git rebase_ with interactive mode to squash multiple commits to one commit.
```text
git rebase -i <commit-hash>
```

<a name="log"></a>
## _Log details of the local commit history_
The _git log_ details out commit histories of current branch.
```text
git log

Flavor:
git log --oneline
```