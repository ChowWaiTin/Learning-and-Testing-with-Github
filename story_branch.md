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
    - Ensure branch is updated
        ```
        git fetch origin
        git pull origin
        ```
    - Create a new branch and navigate to the branch
        ```
        git checkout -b food/locations
        ```
    - Publish branch in the remote repository in order to share with other developers. This will create a new remote branch.
        ```
        git push -u origin food/locations
        ```

2. Developer B decided to work independently from Developer A. In order to achieve this, he decided to create another branch out of the food/locations branch.

    Developer created a new branch as follows:
    - pull newly created remote branch using
    ```
    git pull <remote_name>  <remote_branch_name>:<new_local_branch_name>
    ```
    ```
    git pull origin food/locations:food/locations
    ```
They decided to work independently to list out the different stores and type of food. Both agreed to store their findings into foodplan.txt.
-> File to use foodplan.txt

2. In the process on working on their food plan, both C and D decided to create their own branches
- Friend C created and switch to the branch food/list_food_C
    ```
    git checkout -b food/list_food_C
    ```
- Friend D created and switch to the branch food/list_food_D

3. Friend C did some research on the internet and came up with a list. He modified the foodplan.txt file as follows:
```
# Food Plan
Restaurant A : 11 Mystreet XXXXX
              Spicy Food
Eatery B : 35 Far street XXXXX
              Local Delights              

```

4. Friend D decided to check a guide book and found some restaurant that interest him. He input his findings into the foodplan.txt.
```
# Food Plan
Restaurant X : 5 Way Street XXXXX
              Mixed Cusine
Eatery N : 15 Fastfood Street XXXXX
              Fast Food   
```

5. Friend C was first to complete his findings and decided to stage his changes and make a commit.  Subsequently, he pushed his changes to a new remote branch
    - Stage all changes
    ```
    git add .
    ```
    - Commit changes
    ```
    git commit -m "List of food"
    ```


6. Friend D took a longer time to read through his guide book. After he was done, he staged his changes and made a commit.

7. While checking the remote branch, he noticed that Friend C has completed his research and decided to combine both of their works. 
    a. To do this, he first pulled the remote branch created by Friend C into a local branch 
    b. Next he merged the branch of Friend C into his branch
    c. He encounter a merge conflict when he was performing the merge as both of them were working on the same file.
    d. He decided to resolve the conflict

8. In the process of resolving the conflict, he realized that there are 4 different scenarios
    - Accept C changes (e.g. because they are the latest)
    - Accept D changes (e.g. because they are more interesting)
    - Accept both changes (e.g. because they are unique)
    - Accept some C and some D (e.g. because no spicy food is allowed)

9. Upon resolving the conflict, Friend D performed  a commit and pushed the changes to his own remote branch