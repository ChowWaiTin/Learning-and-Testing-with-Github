# Quick Summary

## Summary
This document is a quick summary on the use of git, a version control tool.

## Example
Try out the example: [Example](./README.md)

There are also some useful info you can refer to below.

---
## Useful Info

1. [Basic Git Commands](#basic-git-commands)
2. [Cloning Repository](#cloning-repository)
3. [Basic Flow - No Merge Conflict](#basic-flow---no-merge-conflict)
4. [Basic Flow - With Merge Conflict](#basic-flow---with-merge-conflict)

## Basic Git Commands
This section provides a list of frequently used git commands. This list is non-exhaustive and does not cover all the git commands.

Subsequent sections will cover some of these commands in greater detail.

Common commands:
- Cloning repository
    ```ps1
    git clone <remote_repo_url (or) ssh>
    ```
- Git Branches (Local)
    ```ps1
    # Listing all branches (local)
    git branch
    
    # Listing all available branches (local + remote)
    git branch -a
    
    # Listing all the remote branches 
    git branch -r
    
    # Create branch
    git branch <new_branch_name>
    
    # Safe delete of local branch (prevent deleting if there are unmerged changes)
    git branch -d <branch_name>
 
    # Force delete of branch (even if it has unmerged changes)
    git branch -D <branch_name>

    # Switch branch
    git switch <branch_name>
    git checkout <branch_name>

    # Create new branch and switch
    git switch -c <new_branch_name>

    # Create a copy of current branch as a new branch and switch to new branch
    git checkout -b <new_branch_name>

    # Rename current branch
    git branch -m <new_name> 

    # Rename a branch
    git branch -m <old_name> <new_name>
    ```
- Git Branches (Remote)
    ```ps1
    # Safe delete of remote branch (example of remote_name -> origin)
    git push -d <remote_name> <branch_name>
    
    # Force delete of remote branch 
    git push -D <remote_name> <branch_name>

    ```
- Add remote connection (Typically remote_name -> origin)
    ```ps1
    add <remote name> <remote https (or) ssh>
    ```
- Fetch / update branch from remote branch
    ```ps1
    # Fetch from default remote name (origin)
    git fetch

    # Fetch from specific remote name
    git fetch <remote_name>

    # Fetch from all remote name
    git fetch -all

    # Force fetch and override local branch (cautious: may overwrite current work)
    git fetch -f <remote_name>

    # Remove any remote-tracking references that no longer exist on the remote before fetching (prune)
    git fetch -p <remote_name>
    ```
- Pulling from remote repository
    ```ps1
    # Pull from remote repository
    git pull <remote_name>
    # e.g. git pull origin

    # Pull specific remote branch to local branch/create branch
    git pull <remote_name> <remote_branch_name>:<new_local_branch>
    ```
- Staging
    ```ps1
    # Adding all to stage
    git add .
    git add -all
    ```
- Committing
    ```ps1
    # Creating a new commit with message
    git commit -m '<commit_message>'

    # Replacing the tip of the current branch with a new commit. This overrides the previous commit
    git commit --amend -m '<commit_message>'
    ```
- Pushing to remote repository
    ```ps1
    # Push the current branch to the remote branch if it has the same name as the current branch (default origin)
    git push <remote_name>

    # Push a local branch to the repository. Branch would be created remotely if it does not exist
    git push <remote_name>  <branch_name>

    # Push current branch to a remote branch matching the name specified
    git push <remote_name> HEAD:<remote_branch_name>
    git push

    # Push current branch and create new branch
    git push -u <remote_name> <create_branch_name>
    ```
- Stashing changes
    ```ps1
    # Stashing all current changes
    git stash

    # Listing all the stashes
    git stash list

    # Retrieve the latest stash
    git stash pop

    # Dropping a specific stash from list
    git stash drop <id>

    # Delete all stash
    git stash clear
    ```

- Updating the local repo to stop tracking deleted remote repo
    ```ps1
    git remote prune <remote_name>
    # e.g. git remote prune origin
    ```
    ```ps1
    git fetch -p
    ```
---
## Cloning Repository
This section covers the cloning of an existing remote repository to a local repository on a local computer. This will require a github account which is granted access to this repository.


---
## Basic Flow - No Merge Conflict
This section covers the basic flow of pulling the source code from a remote repository, making modifications, pushing the modifications to the remote repository and creating a pull request

1. Fetching And Pulling From Main Branch
2. Creating Local Branch and Publishing Branch
3. Modifications, Staging and Committing
4. Fetching And Pulling From Main Branch
5. Merging Repositories 
6. Pushing To Remote Branch
7. Pull Request

---
## Basic Flow - With Merge Conflict
This section covers the basic flow of pulling the source code from a remote repository, making modifications and handling merge conflicts, pushing the modifications to the remote repository and creating a pull request

1. Fetching And Pulling From Main Branch
2. Creating Local Branches 
3. Modifications, Staging and Committing In Different Branches
4. Fetching And Pulling From Main Branch
5. Merging Repositories 
6. Handling Merge Conflicts
7. Pushing To Remote Branch / Publishing Branch
8. Pull Request