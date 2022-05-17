# Version Control System
Version control, also known as source control, is the practice of tracking and managing changes to software code. 
Version control systems are software tools that help software teams manage changes to source code over time.

# Advantages of version control system
- collaboration
- Changes can be tracked easily
- Provides backup
- Easy rollback
- Reduce downtime

# Types of Version control systems
1. Local VCS
2. Central Version Control System, Ex: svn
3. Distributed/Decentralized Version Control System, Ex: Git, Bitbucket

# Centralized vs Distributed VCS
![](Pasted%20image%2020220508125457.png)
**Centralized**  vcs code is directly committed to the remote server.
so offline commits are not possible.

**Distributed** vcs each developer will have a local copy of the repo also reffered to as local repo and commits are initially updated to local repo and its further merged with remote repo.

# Git and Github
**Git** is a Distributed Version Control tool which handles small as well as large projects with efficiency. It is basically used to store our repositories in remote server such as GitHub.

![](Pasted%20image%2020220508130145.png)


**Github** is a hosting service for your repositories. 
A repository(or a repo) is a directory or storage space where your projects live. It can be local to a folder on your computer, or it can be a storage space on another online host (such as Github). You can keep code files, text files. image files. you name it, inside a repository.

![](Pasted%20image%2020220512234119.png)


## Git features
- Economical - its released under GPL license. its free and open source.
- Non-linear - supports non-linear(parallel) development of the software.
- Snapshot - Records changes made to a file rather than file itself.
- Distributed 
- Speed
- Robust - Nearly every task in git is undoable.
- Integrity - Every change can be tracked.

## Git workflow
![](Pasted%20image%2020220508131107.png)
![](Pasted%20image%2020220508131325.png)


## Public vs Private Repo

1.  If original private repo deleted:  all of its forks will be deleted.
2.  If original public repo deleted:  its forks will not be deleted.

When you delete a public repository, one of the existing public forks is chosen to be the new parent repository. All other repositories are forked off of this new parent and subsequent pull requests go to this new parent.

1.  If public repo is converted to private, and deleted the original:  
    Forked repo will not be deleted. a public repository's forks will remain public in their own separate repository network even after the parent repository is made private.

So, If you fork from a public repo, forked repo will not be deleted. If you fork from private repo, forked repo will be deleted.

## Index or staging area
The Git index is a staging area between the working directory and repository. It is used to build up a set of changes that you want to commit together.

Although, Git doesn't have a dedicated staging directory where it can store some objects representing file changes (blobs). Instead of this, it uses a file called index.

## Branch
These branches are a pointer to a snapshot of your changes.
A branch is a version of the repository that diverges from the main working project
When you want to add a new feature or fix a bug, you spawn a new branch to summarize your changes.

## Master branch
The master branch is a default branch in Git. It is instantiated when first commit made on the project. When you make the first commit, you're given a master branch to the starting commit point. When you start making a commit, then master branch pointer automatically moves forward. A repository can have only one master branch.

Master branch is the branch in which all the changes eventually get merged back.

## Rebase
Updates the base branch of the current branch, with the new commits in the base branch.

## Pull request
Notifies developers about changes you've pushed to a branch in a repo.
Acknowledge and review changes
you can create pull requests in two ways.
  - From with in the branch
  - From a forked repo

## Fork
- Copy of other repository. Allows you to freely experiment your changes without affecting original project.
- Bridge between original repository and personal copy
- Core of social coding (open source) at GitHub. Most commonly, forks are used to either suggest changes to someone else's project or to use someone else's project as a beginning point for your own idea.
- Best example of using forks to propose changes is for bug fixes where you fork repository fix issues and raise pull request to merge in original branch.

## Merge conflict
Merge conflicts arise when two files having same content modified, are merged.

![](Pasted%20image%2020220513215938.png)

## Resolving merge conflicts
Merge Conflicts are resolved manually by users
Git provides different Merge-Tools to compare and choose the required changes
User can also use third party Merge-Tools with Git

**Example of merge tool kdiff3**
`git config --global merge.tool kdiff3`
`git mergetool` # this will open the merge tool GUI

## Stashing
save the uncommitted changes and untracked files temporarily, and gives a clean working dir.

**Note**: you can not switch between branches with uncommited changes.

`git stash`
`git stash list`
`git show stash`
`git stash pop`
`git stash apply`

## Rebase
- gives a clean commit history


**Never rebase a public repo**

`git rebase -i master`

**How to undo a rebase ?** by using `reflog`

## Git merge vs rebase
![](Pasted%20image%2020220514165948.png)

![](Pasted%20image%2020220514170046.png)

![](Pasted%20image%2020220514170200.png)

![](Pasted%20image%2020220514170316.png)

![](Pasted%20image%2020220514170357.png)
![](Pasted%20image%2020220514170721.png)

which one is better
![](Pasted%20image%2020220514170820.png)


# Git operation
Create a new local repo
`git init`

Status of the files changed and the files yet to be committed
`git status`

Clone a remote repo
`git clone <url>`

Add one or more files to staging area
`git add`

Commit the changes
`git commit`

Push the changes to master branch
`git push origin master`

Archive the repo
`git archive master --format=zip -output=../nameoffile.zip`

Bundle your repo
`git bundle create ../repo.bundler master`

Stash uncommitted changes
`git stash`
`git stash apply`

# Workflow
What is work flow
- series of tasks
- control sequence of events
- workflow is a change management
## Git flow vs Github flow
![](Pasted%20image%2020220513211155.png)
