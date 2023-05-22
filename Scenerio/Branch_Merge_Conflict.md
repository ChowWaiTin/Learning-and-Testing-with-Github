## Summary
1. A create branch C1
2. B create branch C2
3. Both working on same feature - plan what to eat
4. A commit and merge to feature branch
5. B commit and merge to feature branch
6. B encounters conflict
7. B resolve conflict
    - Accept C changes
    - Accept D changes
    - Accept both changes
    - Accept some C and some D
8. B commit the merge
9. B push changes to feature branch


## Storyline
1. Developer A and B decided to begin planning for their food by listing the different food outlets available. They decided that they did not want to mix their food planning with their literary planning. In order to do so, they decided to create another branch from the main branch.

    Developer A created a new branch as follows:
    - Switch to main branch
        ```
        git switch main
        ```
        Expected response:
        ```
        Switched to branch 'main'
        Your branch is up to date with 'origin/main'
        ```
    - Ensure branch is updated
        ```
        git fetch origin
        git pull origin
        ```
    - Create a new branch and navigate to the branch
        ```
        git checkout -b food/locations
        ```
        Expected response:
        ```
        Switched to a new branch 'food/locations'
        ```
    - Publish branch in the remote repository in order to share with other developers. This will create a new remote branch.
        ```
        git push -u origin food/locations
        ```

2. Developer B decided to work independently from Developer A. In order to achieve this, he decided to create another branch out of the food/locations branch.

    Developer B created a new branch as follows:
    - Checks all the branches with `git branch -a`
        ```ps1
        # Check all branch
        git branch -a
        ```
    - Pull newly created remote branch using with `git pull <remote_name>  <remote_branch_name>:<new_local_branch_name>`
        ```
        git pull origin food/locations:food/locations
        ```
    - Switch to the branch with `git switch <branch_name>`
        ```
        git switch food/locations
        ```
    - Create a new branch with `git checkout -b <new_branch_name>`
        ```
        git checkout -b food/locations_dev_B
        ```
    - Publish branch to remote repository
        ```
        git push -u origin food/locations_dev_B
        ```

3. Developer B obtained a list of food outlets using the internet. After searching for the required information, he decided to update the foodoutlet.txt file.

    - Developer B update the file: foodoutlet.txt
        ```
        # Food Outlets
        Meiji Shrine area: Kagari Ramen, Harajuku Gyoza Lou, or Gyukatsu Motomura
        Tokyo Skytree: Sky Restaurant 634, Sumida Aquarium Café & Restaurant, or Soranoiro Nippon            
        ```

4. Upon completion of his task, Developer B decided to stage his changes, make a commit. He subsequently push his changes to his remote branch (food_locations_dev_B) as his task was completed

    - Stage change
        ```
        git add .
        ```
    - Commit
        ```
        git commit -m "Added a list of food outlets"
        ```
    - Update remote repository
        ```
        # Check for updates
        git pull origin
        # Push his changes
        git push origin
        ```

5. While Developer B was creating a list of food outlets, Developer A was also working on a similar task. However, he chose to research the list through guide books and took a little longer to complete his list. Upon completion of his research, he decided to update the foodoutlet.txt file.

    - Developer A update the file: foodoutlet.txt
        ```
        # Food Plan
        Fushimi Inari Shrine: Udon Yamaokaya, Inari No Chanya, or Sushi Mamire
        Gion district: Gion Kappa, Gion Nanba, or Gion Tokuya 
        ```

6. Upon completion of his task, Developer A decided to stage his changes, make a commit. He subsequently pushed his changes to the food/locations repository

    - Stage change
        ```
        git add .
        ```
    - Commit
        ```
        git commit -m "Added a list of food outlets"
        ```
    - Update remote repository
        ```
        # Check for updates
        git pull origin
        # Push his changes
        git push origin
        ```

7. After having updated the remote repository with his list, Developer A saw a message from Developer B indicating that the latter has updated a list of his own in a separate repository. He decided to merge the information in order to create a complete list.

    - Pull newly created remote branch using
        ```
        # This creates a local branch from the remote branch
        # git pull <remote_name>  <remote_branch_name>:<new_local_branch_name>
        git pull origin food/locations_dev_B:food/locations_dev_B
        ```
    - Merge the branches (currently in food/location)
        ```
        git merge food/location_dev_B
        ```

8. Upon merging, Developer A encountered conflict as they had updated the same file. He proceed to begin the conflict resolution and realized that there are 4 different ways he can do so:
    - Accept Developer B changes and discard Developer A changes
    - Accept Developer A changes and discard Developer B changes
    - Accept both changes
    - Accept some changes of Developer A and some from Developer B

9. After resolving all the changes, Developer A created a commit to finalize the merge. The result of the merge is in food/location branch.


## Lesson Learnt
1. Recap branch creation and publishing branch to remote repository

2. Recap basic flow of any updates

3. Understand branch merger

4. Understand conflicts during branch merger

5. Understand conflicts resolution.