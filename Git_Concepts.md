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


**Github** is a central repository or simply a repo.
A repository(or a repo) is a directory or storage space where your projects live. It can be local to a folder on your computer, or it can be a storage space on another online host (such as Github). You can keep code files, text files. image files. you name it, inside a repository.

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

## Branch

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