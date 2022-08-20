# Install Git
## Centos 7
`sudo yum install git -y`

https://www.digitalocean.com/community/tutorials/how-to-install-git-on-centos-7
Check the version: `git --version`

## Windows 10
Git bash - CLI (All the linux commands works in gitbash shell)
Git desktop - GUI
    Useful with obsidian


# Check out a single file from remote repo
1. Add remote repo
    ```sh
    git remote add repo1 <repoURL>
    ```
2. Fetch it
   ```sh
   git fetch repo1
   ```
3. Check out a file
   ```sh
   git checkout repo1/master -- vars/gitSSHCheckout.groovy
   ```
   
   > Note: make sure ur on main branch folder within `gitbash/shell`

# Working with Repositories
## Initialize an empty repo on to your filesystem
1. Create a dir and add files to track
    ```sh
    mkdir devops
    cd devops
    echo "file A" > fileA.txt
    echo "file B" > fileB.txt
```
2. Initialize the repo
    `git init` # Initializes an empty repo, creates .git dir.
3. Add files to the repo
    `git add .`
    `git status`
4. Commit the changes
    `git commit -m "Initial commit"`
5. Check the status or log
    `git status`
    `git log`

![](Pasted%20image%2020220718132840.png)

## Git configuration
```sh
git config list
git config --global user.name "User Name"
git config --global user.email "email@gmail.com"
```

## Make changes for the files
1. Modify/Update a file
2. Add file to staging area
    `git add <file.txt>`
3. Check the status
    `git status`
1. Commit the changes
    `git commit -m "commit message"`

## Restore files to previous commit version
1. List the version or commits
    `git log`
    `git log -all` # List all the commits
2. Restore
    `git checkout <commitID>`

```sh
git add
git restore # To discard changes in Working directory
git commit -a
git diff
```

## Unstage a file/changes
`git rm --cached <file1>`
check out `git restore --staged <file1>` and `git reset`

## Push changes to remote repo
```sh
git remote add origin https://github.com/alashro/devops.git
git branch -M main
git push -u origin main
```

```sh
git push --all origin # will push all the branches too
git push origin # pushes only the master branch changes
```
## Clone a repo
```sh
 git clone https://username@bitbucket.org/teamsinspace/documentation-tests.git
 git clone ssh git@github.com:bhaaskara/hello-world.git
```



# Creating personal access token github
https://docs.github.com/en/enterprise-server@3.4/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token


# Remote Repos
## Add a remote Repo
```sh
git remote add <rigin/alias> URL(https://github.com/bhaaskara/git.git)
```

## List the remote repos
 `git remote -v`

## Rename the alias
`git remote rename origin repo1`
## Change remote repo
 ```sh
 git remote set-url <an-existing-remote-name> <url>`
```

## Delete a remote repo
 ```sh
 git remote delete <alias/origin>`
```

# Clone a repo
## Gitbash / Linux CLI
 **Over https**  
```sh
 git clone https://username@bitbucket.org/teamsinspace/documentation-tests.git
```
 
**Over ssh**
```sh
 git clone ssh://git@bitbucket.org:teamsinspace/documentation-tests.git
```

## Clone a repository with VS Code
You can also use Visual Studio (VS) Code to clone your repository. If you aren't familiar with VS Code, it's a source code editor developed by Microsoft that provides an alternative to the command line. Follow these instructions to clone your repository. If you don't have Visual Studio Code, [download the application first](https://code.visualstudio.com/download "https://code.visualstudio.com/download").

1.  From the repository, select the **Clone** button.
2.  In the **Clone this repository** dialog, select the **Clone in VS Code** button.
    
    1.  If you have not already installed the [Atlassian for VS Code extension](https://marketplace.visualstudio.com/items?itemName=Atlassian.atlascode "https://marketplace.visualstudio.com/items?itemName=Atlassian.atlascode"), you will be prompted to install it. Select **Install** > select the **Reload Window and Open** button in the info dialog.
        
3.  In VS Code, select **Clone a new copy** from the dropdown menu.
    
4.  When prompted, select the local storage location where you want to keep the cloned repository. 
    
5.  Select the **Select repository location** button.
    
6.  Your repository will be cloned and stored in the location you chose. You can then open the repository and begin working on it in VS Code.

# Git operations
![](Pasted%20image%2020220508132809.png)
![](Pasted%20image%2020220508131325.png)


`git init` : Initializes a new empty local repository
`git clone` : Creates a copy of the original repository from Github on local machine.
`git fork` : Creates a copy of the original repository on your github account.

`git remote add origin <repo_url>` : Add a remote repo on your local machine
`git pull origin master` : Copy all the files from master branch of remote repo to your local repo
`git push origin master` : Push your local changes into central remote repo

## Create a new local repo
ref: https://docs.github.com/en/get-started/importing-your-projects-to-github/importing-source-code-to-github/adding-locally-hosted-code-to-github


```
1. Create a directory
2. Initialize the new repo (Dir can have files/no need to be empty)
3. Configure the user details
```

1. Configure git global values 
  ```
  git config --global user.name "test user"
  git config --global user.email "testemail@email.com"
  ```
2. Create a directory
    `mkdir <test_repo>`
    `cd <test_repo>`
3. Initialize the new repo
    `git init`
4. Check the status
    `git status` 
5. Add the file to staging area, git starts tracking the changes
    `git add <file>`

    Note: `git rm --cached <file>` to unstage
6. Commit the changes to the local repo, it commits all the files
    `git commit -m "commit message"`
7. List all the commits
    `git log`
8. show the changes with in a commit
    `git show "commit ID"`

## Sync the changes with Remote repo
1. Add a remote repo
    `git remote add origin https://github.com/bhaaskara/git.git`
    Note: To create a new repo from cli use GitHub cli - `gh`
2. Push the changes to remote repo
    ``
# Working with Branches
1. Create a branch
    `git branch <feature>`
2. Checkout the branch
    `git checkout <feature>`

Note: at any point of time you can switch to any branch using `git checkout`

## Merging
### Implicit or fast forward merge
This is the simplest merging method.

You create a branch(named feature) out of Master.
Made changes/commits in the new branch.
Merge the Branch with Master
During this time no changes made to the master.

Note: when you want to merge feature branch with master branch
          check out to master branch
          merge with feature branch
          
![](Pasted%20image%2020220718185217.png)

### Explicit/Recursive/3-way Merge
You create a branch(named feature) out of Master.
Made changes/commits in the new branch.
Changes happened in master also in parallel.
This Merge is called as a Recursive merge and this creates a new commit on the master to merge.
This copies all the feature branch history and commit message on to master branch history
![](Pasted%20image%2020220718191227.png)

### Squash merge
This is used to condense the git history of the feature branches when a merge is 
carried Out. 
Here instead Of each commit history of the feature branch being added to the 
commit history of the master branch, the squash merge will take all the file 
changes and then just create one single new commit on the master branch. 
This helps to keep the commit history clean when it comes to the master branch.

`git merge --squash <featureBranchName>`

# Merge conflict
When a merge conflict happens `git merge`  will shows the files with the conflicts

Then open the file in master branch and keep the changes you need
![](Pasted%20image%2020220719105153.png)
after edit
![](Pasted%20image%2020220719105244.png)

Then commit
```sh
git add .
git commit -m "conflict resolved"

```

**Note:** To leave the changes and to start fresh you can use `git merge --abort` or `git rebase --abort` 
# Pull changes from Git repo
`git pull`
