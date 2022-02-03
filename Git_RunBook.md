# Check out a single file from remote repo
1. Add remote repo
    `#git remote add repo1 <repoURL>`
2. Fetch it
   `git fetch repo1`
3. Check out a file
   `git checkout repo1/master -- vars/gitSSHCheckout.groovy`
 > Note: make sure ur on main branch folder within gitbash/shell

# Remote Repos
 ## Add a remote Repo
 `git remote add <local_repo_name> <URL (https://github.com/bhaaskara/git.git)>`

 where `<local_repo_name>` is a unique remote name.

 ## List the remote repos
 `git remote -v`

 ## Change remote repo
 `git remote set-url <an-existing-remote-name> <url>`

 ## Delete a remote repo
 `git remote delete <local_repo_name>`

 # Clone a repo
 Over https
 `git clone https://username@bitbucket.org/teamsinspace/documentation-tests.git`

 Over ssh
 `git clone ssh://git@bitbucket.org:teamsinspace/documentation-tests.git`

 ## Clone a repository with VS Code

You can also use Virtual Studio (VS) Code to clone your repository. If you aren't familiar with VS Code, it's a source code editor developed by Microsoft that provides an alternative to the command line. Follow these instructions to clone your repository. If you don't have Visual Studio Code, [download the application first](https://code.visualstudio.com/download "https://code.visualstudio.com/download").

1.  From the repository, select the **Clone** button.
2.  In the **Clone this repository** dialog, select the **Clone in VS Code** button.
    
    1.  If you have not already installed the [Atlassian for VS Code extension](https://marketplace.visualstudio.com/items?itemName=Atlassian.atlascode "https://marketplace.visualstudio.com/items?itemName=Atlassian.atlascode"), you will be prompted to install it. Select **Install** > select the **Reload Window and Open** button in the info dialog.
        
3.  In VS Code, select **Clone a new copy** from the dropdown menu.
    
4.  When prompted, select the local storage location where you want to keep the cloned repository. 
    
5.  Select the **Select repository location** button.
    
6.  Your repository will be cloned and stored in the location you chose. You can then open the repository and begin working on it in VS Code.