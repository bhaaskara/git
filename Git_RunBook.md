# Install Git
## Centos 7
`sudo yum install git -y`

https://www.digitalocean.com/community/tutorials/how-to-install-git-on-centos-7

## Windows 10
Git bash - CLI
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

