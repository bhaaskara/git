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
2. Central Version Control System, Ex: Subversion, CVS, Perforce, Teamfoundation version control
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

## .git Directory
- Local database
- Maintains entire history of your changes
- Contains information on the commits, remote repo address

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

## Head and Origin
![](Pasted%20image%2020220718184743.png)
**HEAD** is a pointer to the current position in the code tree, and in this example its pointing to feature branch.
**Origin/master** is a pointer to the remote repo in the code tree. Here it shows that your remote repo is pointing to the second commit.
**master** is a pointer to the master branch of the local repo and here both local master and remote master are at the same point.

## Rebase
Updates the base branch of the current branch, with the new commits in the base branch.

## Pull request
Notifies senior developers/lead about changes you would like to pushed to a branch in a repo.
Acknowledge and review changes

you can create pull requests in two ways.
  - From with in the branch
  - From a forked repo

Note: Push is directly push your changes to the master while pull request gives a control over pushing your changes by giving an option to review the changes before merging.


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
- Rebasing is **a process to reapply commits on top of another base trip**. It is used to apply a sequence of commits from distinct branches into a final commit. It is an alternative of git merge command. It is a linear process of merging.


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

## Tag
Tags are ref's that point to specific points in Git history. Tagging is generally used to capture a point in history that is used for a marked version release (i.e. v1.0.1). A tag is like a branch that doesn’t change. Unlike branches, tags, after being created, have no further history of commits.

Git supports two different types of tags, annotated and lightweight tags. they differ in the amount of accompanying meta data they store. 
**A best practice is to consider Annotated tags as public, and Lightweight tags as private.** Annotated tags store extra meta data such as: the tagger name, email, and date. This is important data for a public release. Lightweight tags are essentially 'bookmarks' to a commit, they are just a name and a pointer to a commit, useful for creating quick links to relevant commits.

`git tag -a "v1.0" -m "this is version 1"`  Create a tag
`git tag` list the tags
`git show v1.0` Details of a tag

## Rewriting history (change commit message)
### Change most recent commit messge
`git commit --amend -m "an updated commit message"`

### Changing committed files
```sh
# Edit hello.py and main.py  
git add hello.py  
git commit   
# Realize you forgot to add the changes from main.py   
git add main.py   
git commit --amend --no-edit
```
The `--no-edit` flag will allow you to make the amendment to your commit without changing its commit message. The resulting commit will replace the incomplete one, and it will look like we committed the changes to `hello.py` and `main.py` in a single snapshot.

### Don’t amend public commits
Amended commits are actually entirely new commits and the previous commit will no longer be on your current branch. This has the same consequences as resetting a public snapshot. Avoid amending a commit that other developers have based their work on. This is a confusing situation for developers to be in and it’s complicated to recover from.

## Branch Protection
![](Pasted%20image%2020220820124144.png)

- allows to add approvals before merging any changes to the branch.
- 
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

Remove any stale objects
`git prune --expire now`

# Git Flow
![](Pasted%20image%2020220719161941.png)
![](Pasted%20image%2020220719161926.png)
![](Pasted%20image%2020220719162102.png)
![](Pasted%20image%2020220719162122.png)
![](Pasted%20image%2020220719162149.png)



You can download and install Git flow
This can be used in addition to your normal git commands.
It can be used to maintain ur branches.

## Git credentials
When accessing Git repositories HTTPS, you need to enter credentials Which 
consists of your user name and password. 
If you don't want to enter your user name and password every time you work 
With Cit repositories, you can use the Git credential system. 
The Git credential System has a cache mechanism that can be used to cache 
your credentials, 
There are different settings when it comes to the cache 
The default setting is not to cache anything at all 
The next cache settings is to keep the credentials in memory for a certain period 
Of time. 
You can also define a setting to save the credentials in a plain-text file on disk

# Workflow
What is work flow
- series of tasks
- control sequence of events
- workflow is a change management
## Git flow vs Github flow
![](Pasted%20image%2020220513211155.png)

# Github enterprise 
Git can be hosted on on-premise server using Github enterprise.