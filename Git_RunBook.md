# Install Git
## Centos 7
`sudo yum install git -y`

https://www.digitalocean.com/community/tutorials/how-to-install-git-on-centos-7

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
## Clone a repo
```sh
 git clone https://username@bitbucket.org/teamsinspace/documentation-tests.git
 git clone ssh git@github.com:bhaaskara/hello-world.git
```

## Modify a file
Modify the files using any of the editors

## Add file to staging area
```sh
git add .  #Adds all the files to staging area
```

## Check the status
```sh
git status # Check the files to be commited
```

## Commit the changes
```sh
git commit -m "commit message"
```

## Push the changes to master/remote repo
```sh
git push origin master
```

# Creating personal access token github
https://docs.github.com/en/enterprise-server@3.4/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token


# Remote Repos
## Add a remote Repo
```sh
git remote add <local_repo_name> URL(https://github.com/bhaaskara/git.git)
```
where `local_repo_name` is a unique remote name.

## List the remote repos
 `git remote -v`

## Change remote repo
 ```sh
 git remote set-url <an-existing-remote-name> <url>`
```

## Delete a remote repo
 ```sh
 git remote delete <local_repo_name>`
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