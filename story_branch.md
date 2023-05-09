## Summary
1. C create branch C1
2. D create branch C2
3. Both working on same feature - plan what to eat
4. C commit and merge to feature branch
5. D commit and merge to feature branch
6. D encounters conflict
7. D resolve conflict
    - Accept C changes
    - Accept D changes
    - Accept both changes
    - Accept some C and some D
8. D commit the merge
9. D push changes to feature branch


## Storyline
1. Friend C and D were assigned to plan for the food. They decided to work independantly to list out the different stores and type of food. Both agreed to store their findings into foodplan.txt.
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
Restraunt A : 11 Mystreet XXXXX
              Spicy Food
Eatery B : 35 Farstreet XXXXX
              Local Delights              

```

4. Friend D decided to check a guide book and found some restraunt that interest him. He input his findings into the foodplan.txt.
```
# Food Plan
```

5. Friend C was first to complete his findings and decided to stage his changes and make a commit.  Subsequently, he pushed his changes to a new remote branch

6. Friend D took a longer time to read through his guide book. After he was done, he staged his changes and made a commit.

7. While checking the remote branch, he noticed that Firend C has completed his research and decided to combine both of their works. 
    a. To do this, he first pulled the remote branch created by Friend C into a local branch 
    b. Next he merged the branch of Friend C into his branch
    c. He encounted a merge conflict when he was performing the merge as both of them were working on the same file.
    d. He decided to resolve the conflict

8. In the process of resolving the conflict, he realised that there are 4 different scenerios
    - Accept C changes (e.g. because they are the latest)
    - Accept D changes (e.g. because they are more interesting)
    - Accept both changes (e.g. because they are unique)
    - Accept some C and some D (e.g. because no spicy food is allowed)

9. Upon resolving the conflict, Friend D performed  a commit and pushed the changes to his own remote branch