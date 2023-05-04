# Learning-and-Testing-with-Github

## Summary
This document covers basics of working with a repository using git commands. 
## Content
1. [Basic Git Commands](#basic-git-commands)
2. Cloning Repository
3. Working With Remote Branches
4. Staging and Commiting
5. Fetching And Pulling 
6. Merging Repositories 
7. Handling Merge Conflicts
8. Pushing To Remote Branch
9. Pull Request

## Basic Git Commands
This section provides a list of frequently used git commands. This list is non-exhaustive and does not cover all the git commands.

Subsequent sections will cover some of these commands in greater detail.

Common commands:
- Cloning repository
    ```ps1
    git clone <remote_branch_url (or) ssh>
    ```
- Git Branches (Local)
    ```ps1
    # Listing all branches (local)
    git branch
    
    # Listing all avaliable branches (local + remote)
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
- Add remote connection
    ```ps1
    git remote add <remote name> <remote https (or) ssh>
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
    git pull origin
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
    git commit --ammend -m '<commit_message>'
    ```
- Pushing to remote repository
    ```ps1
    # Push the current branch to the remote branch if it has the same name as the current branch (default origin)
    git push <remote_name>

    # Push a local branch to the repository. Branch would be created remotely if it does not exist
    git push <remote_name>  <branch_name>

    # Push current branch to a remote branch matching the name specified
    git push <remote_name> HEAD:<remote_branch_name>
    ```
- Stashing changes
    ```ps1
    # Stashing all current changes
    git stash

    # Listing all the stashes
    git stash list

    # Retrive the latest stash
    git stash pop

    # Droping a specific stash from list
    git stash drop <id>

    # Delete all stash
    git stash clear
    ```

## Cloning repository
This section covers the cloning of an existing remote repository to the local computer.




