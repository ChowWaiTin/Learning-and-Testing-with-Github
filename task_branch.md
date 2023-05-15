## Summary
1. A create branch A
2. B create branch B
3. B decided to help A on the branch A
4. B commit and push changes to branch A
5. A commit and push changes to branch A
6. A encounters conflict
7. A resolve conflict
    - Decide what changes to accept
8. A commit the merge
9. A push changes to branch A

## Storyline
1. Friend A edits text file for Day 1 itinerary. While planning the schedule,
he has difficulty choosing between one of the two places.
2. Friend B decides to help, so he checkout friend A's branch.
    a. Firstly he typed out `git branch --all` to list out the branches that have been created on the repository.
    b. Once he knows friend A's branch to checkout, he typed out `git switch {friend's A branch name} or git checkout {friend's A branch name}`.
3. Both of them ended up working in the same branch, on the same file.
4. Friend B finished editing the file and pushes the edit.
    a. Firstly he needs to `git pull` on the branch itself.
    b. Next he can stage his changes and commit it with `git add .` .
    c. Then followed by `git commit -m "insert commit message" `.
    d. After that he `git push` his changes to the branch.
5. At the same time, friend A also made some changes to the file and pushes the edit.
6. Conflict happens depending on who pushed later. (Friend A encountered the conflict)
    a. The person who pushed the changes after will experience a conflict.
7. In the process of resolving the conflict, he has to ensure that Friend B's work does not overwrite his own work and vice versa.
    a. In this scenario, he has to carefully look through line by line at both Incoming Changes and Current Changes.
    b. Then decide what changes to accept and merge accordingly.
8. Upon resolving the conflict, Friend A performed a commit and pushed the changes to his own remote branch. 
9. Finally, he can merge his branch to the main branch so Friend B can see his changes he made to the itinerary.

## Summary
1. A creates branch A
2. A commit and push changes to branch A
3. A push changes to branch A
4. A merge branch to main branch

## Storyline
1. Friend A is tasked to come up with the itinerary for day 1.
    a. Firstly, he creates a branch with `git branch {branch name}`
2. He edits the text file for Day 1 itinerary and saved the file locally.
    a. Worked on the text file on the branch he created.
3. So in order to share it with the group, he has to "push" the updates into the repository.
    a. Once done editing the text file, he `git add . `
    b. Next `git commit -m "insert commit message" `
    c. Then followed by `git push` the changes to his branch
    d. Lastly, he can merge his branch to the main branch