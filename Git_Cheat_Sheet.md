# Global values/variables
Usage | Command
:-- | :--
List the values | `git config --list`
 | | `git config --get user.name`
 | | ` git config --list --name-only`
set user name | `git config --global user.name "testuser"`
Set email | `git config --global user.email "testemail@email.com"`



Usage | Command
:-- | :--
Commit | `git commit -m "message"`
List of commits | `git log`
Details of a commit | `git show "commit DID"`
Revert a commit | `git revert <commitID/message>`
Initializes a new empty local repository | `git init` 
Clone a repo | `git clone` 
fork a repo | `git fork` 
Files tracked by git | `git ls-files`
add remote repo | `git remote add origin https://github.com/bhaaskara/git.git`
List remote repos | `git remote -v `

# Branch
Usage | Command
:-- | :--
List all branches | `git branch`
create a branch | `git branch <branch_name>`
