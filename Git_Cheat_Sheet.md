# Global values/variables
Usage | Command
:-- | :--
Git version | `git --version`
List the values | `git config --list`
 | | `git config --get user.name`
 | | ` git config --list --name-only`
set user name | `git config --global user.name "testuser"`
Set email | `git config --global user.email "testemail@email.com"`
Set user name only for current repo | `git config user.name "testuser"`
Set email only for current repo | `git config user.name "testuser"`



Usage | Command
:-- | :--
Current status | `git status`
Commit | `git commit -m "message"`
List of commits | `git log`
 | | `git log <branch name>`
  | | `git log --oneline`
Details of a commit | `git show "commit DID"`
Revert a commit | `git revert <commitID/message>`
Initializes a new empty local repository | `git init` 
Clone a repo | `git clone <https://github.com/bhaaskara/test.git>` 
fork a repo | `git fork` 
Files tracked by git | `git ls-files`
add remote repo | `git remote add origin https://github.com/bhaaskara/git.git`
List remote repos | `git remote -v `

# Branch
Usage | Command
:-- | :--
List all branches | `git branch` or `git branch --list`
create a branch | `git branch <branch_name>`
Switch to a branch | `git checkout <branch_name>`
Create and switch | `git checkout -b <branch_name>`
Rename a branch | `git branch -m <branch_name> <new_Branch_name>`
Push the changes to remote repo | `git push -u origin master`
merge changes with master branch | `git checkout master` <br/>`git merge <brnach_name>`
Delete a branch in local repo | `git branch -d <branch_name>` #only merged branches can be deleted
  | | `git branch -D <branch_name>` # unmerged branches 
Delete a remote branch | `git push origin -delete <branch_name>`
rebase | `git rebase master` 

## Compare
Usage | Command
:-- | :--
Compare files <br/> Compares with staged file| `git diff <file>`
Compare with remote repo | `git diff --cached <file>`
Compare two files | `diff <file1> <file2>` #Unix command
compare commits | `git diff <commitID1> <commitID2>`
compare commit with file | `git diff <commit ID> <file>`

compare local and remote branch
![](Pasted%20image%2020220513145014.png)

`git revert <commitID>`
`git revert HEAD` # Reverts last commit

`git log`
`git log --all`
`git log --graph`
`git log --graph --decorate --oneline`