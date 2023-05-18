# Learning Git with Real-Life Applications

## Context of Real-Life Application
A group of developers decided to go on vacation trip together after their recent project has been deployed and commisioned. The lead developer of the developement team decided to use GitHub to store the details of their vacation trip such as the itenary, budget planning and etc.

## 1. Setting up the Pre-requisites
Before the team of developers can plan for their trip, the lead developer would need to ensure that the team would have the following things required:

- Having [Git Installed](./1.%20Setting%20up%20the%20Pre-requisites/Git%20Bash%20(Windows)%20Tutorial.mkv) on their Local Device
- Having a [GitHub Account]

## 2. Getting Started - Initialise a Repository for the Project (Create a Shared Folder for Collaboration)

Before the gathering the team together to plan for the trip, the lead developer would need to create a **central shared folder** where the team can collaborate together to plan for the trip. In GitHub, this shared folder is a **central repository** that the developers will be collaborating in.

To have a central repository for collaboration, the lead developer would need to initalise a repository for the team to plan the trip.

To do so, the lead developer would need to:

1. [Configure Global Setting for Git](./2.%20Getting%20Started/1._Git_Configure_Global_Settings.md)

    *  This is to allow you to set default values for your user identity and preferred behaviors across all Git repositories on your development machine. 

2. [Initialise (Create) A Remote Repository on GitHub Webpage](./2.%20Getting%20Started/2._Create_Remote_Repo.md)

    * This is to allow the team to store the information of their trip on the remotely

3. [Adding Collaborators](./2.%20Getting%20Started/3._Add_Collaborators.md)

    * This is to allow the team to be able to collaborate and plan together for the trip

4. [Initialise (Create) A Local Git Repository on Local Device](./2.%20Getting%20Started/4._Create_Local_Repo.md)

    * This repository (file folder) will contain all the files and folders associated with the planning of the vacation trip.

5. [Making Initial Commits (Initialise Initial Files) for Local Git Repository](./2.%20Getting%20Started/5._Initial_Files_Local_Repo.md)

    * Add Initial Files to Local Git Repository
    * Commit the Changes to Local Git Repository

6. [Connect Local Git Repository to Global Git Repository](./2.%20Getting%20Started/6._Remote_to_Local_Repo.md)

7. [Push Changes to Global Git Repository](./2.%20Getting%20Started/7._Push_Global_Repository.md)

## 3. Getting Started - Begin Collaborating (Cloning Global Repository to Local Device)
To begin collaborating to plan the trip together, the developers can start by cloning the global repository into their local device.

For the steps on how to clone the global repository and find out more, [click here](./3.%20Clone%20Repo%20To%20Start%20Collaborating//1._Clone_Repo.md)! 

## 4. Planning for the Trip - Collaboration

## Storyline 1 (Xun)
1. Developer A is tasked to come up with the itinerary for day 1.
    a. Firstly, he creates a branch with `git branch itinerary/activities`.
2. Followed by switching to the branch he created with `git switch itinerary/activities`.
2. He created a text file named `itenerary.txt` and saved the file locally.
3. So in order to share it with the group, he has to "push" the updates into the repository.
    a. Once done editing the text file, he `git add .`
    b. Next `git commit -m "added itinerary text file" `
    c. Then followed by `git push` the changes to his branch
4. Lastly, he merge his branch to the main branch by checking for any changes in the main branch.
    `git switch main`
    `git fetch`
    `git pull`
    `git switch itinerary/activities`
    `git merge main`
    `git switch main`
    `git merge itinerary/activities`
    `git push`
    Switch back to his own branch and publish the branch along with his changes to the remote repository.
    `git switch itinerary/activities`
    `git push -u origin`
    

## Storyline 2 (Xun)
1. Developer A edits text file `itinerary.txt` for Day 1 itinerary. While planning the schedule,
he has difficulty choosing between one of the two places.
2. Developer B decides to help, so he checkout Developer A's branch.
    a. Firstly he typed out `git branch --all` to list out the branches that have been created on the repository.
    b. Once he knows Developer A's branch to checkout, he typed out `git switch {Developer's A branch name} or git checkout {Developer's A branch name}`.
3. Both of them ended up working in the same branch, on the same file.
4. Developer B finished editing the file and pushes the edit.
    a. Firstly he needs to `git pull` on the branch itself.
    b. Next he can stage his changes and commit it with `git add .` .
    c. Then followed by `git commit -m "insert commit message" `.
    d. After that he `git push` his changes to the branch.
5. At the same time, Developer A also made some changes to the file and tries to push the edit.    
    a. He stage his changes and commit it with `git add .` .
    b. Then followed by `git commit -m "insert commit message" `.
    c. After that he `git push` his changes to the branch.
6. Conflict happened for Developer A since he is pushing his changes later.    
7. In the process of resolving the conflict, he has to ensure that Developer B's work does not overwrite his own work and vice versa.
    a. In this scenario, he has to carefully look through line by line at both Incoming Changes and Current Changes.
    b. Then decide what changes to accept and merge accordingly.
8. Upon resolving the conflict, Developer A performed a commit and pushed the changes to his own remote branch. 
9. Finally, he can merge his branch to the main branch so Developer B can see his changes he made to the itinerary.

## Storyline 3 (Bao Jin)
1. Developer A and B continues to work on the itinerary. Both of them worked within the itinerary/activities branch. Developer A found a number of interesting activities and stored them in the **activities.txt** file

    - Developer A checks the branches
        ```ps1
        # Check all branch
        git branch -a
        ```
        The response should show the following:

        If branch is missing, please ensure that the previous task has been completed.

    - Developer A switch to the itinerary/activities branch
        ```ps1
        # Switching branch
        git switch itinerary/activities
        ```
    - Developer A added modifications
        ```
        # Activities file
        Visit the Meiji Shrine - A beautiful Shinto shrine located in the heart of Tokyo's bustling Shibuya district

        Lake Ashi - Relaxing boat ride 
        ```

2. Meanwhile, Developer B found that it was better to place the information on the activities together with the itinerary plan in the itinerary.txt file. After some discussion with the team, he began the process of transferring the information and deleted the activities.txt file. This change was not made aware to Developer A.

    - Developer B checks the branches
        ```ps1
        # Check all branch
        git branch -a
        ```
        The response should show the following:

        If branch is missing, please ensure that the previous task has been completed.

    - Developer B switch to the itinerary/activities branch
        ```ps1
        # Switching branch
        git switch itinerary/activities
        ```

    - Developer B modified itinerary.txt 


3. After completing the update on the activities.txt file, Developer A staged his changes, made a commit and pushed the changes to the remote repository.

    - Developer A stage changes
        ```
        git add .
        ```
    - Developer A commits
        ```
        git commit -m "Added new activities to activities.txt"
        ```
    - Developer A pull and push changes
        ```
        # fetch the latest changes
        git fetch origin
        # pull latest changes from repository
        git pull origin
        # push the update
        git push origin
        ```

4. At the same time, Developer B completed the transfer of the information and deleted activities.txt file. He staged his changes and made a commit. Before pushing his changes to the remote repository, he updated his local repository and found a conflict.

    - Developer B deletes the activities.txt
    - Developer B stage changes
        ```
        git add .
        ```
    - Developer B commits
        ```
        git commit -m "Transfer activities info to itinerary.txt. Delete activities.txt."
        ```
    - Update local repository with remote repository
        ```
        # fetch the latest changes
        git fetch origin
        # pull latest changes from repository
        git pull origin
        ```
    - Encounters a conflict. The file he deleted had changes

5. Developer B subsequently moved the additional information to the itinerary.txt file and made a commit

    - Proceed to resolve the conflict 
    - Transfer new changes to itinerary.txt
    - Delete activities.txt
    - Perform a commit
        ```
        git commit -m "Resolve conflict from deleted activities.txt"
        ```

6. Developer B pushed his changes to the remote repository and proceed to inform Developer A of this change.
    
    - Developer B pushes the changes to remote repository
        ```
        git push origin
        ```


## Lesson Learn
1. Potential conflicts from file deletion and how to handle it.

2. Reminder to fetch and pull changes from remote repository before pushing changes.


## Storyline 4 (Bao Jin)
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

    Developer B created a new branch as follows:
    - Pull newly created remote branch using:
        ```
        # This creates a local branch from the remote branch
        # git pull <remote_name>  <remote_branch_name>:<new_local_branch_name>
        git pull origin food/locations:food/locations
        ```
    - Switch to the branch
        ```
        git switch food/locations
        ```
    - Create a new branch
        ```
        git checkout -b food/locations_dev_B
        ```
    - Publish branch to remote repository
        ```
        git push -u origin food/locations_dev_B
        ```

3. Developer B decided to create a list of food outlets using the internet. After searching for the required information, he decided to update the foodoutlet.txt file.

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

## Storyline 5:
After experiencing so many merge conflicts, they decided to implement pull requests as a solution.

1. Individual branches pull and merge from main to ensure no conflicts.
2. Individual branches merge their changes into main and send a pull request.
3. Developer A then follows to review the requests and accept/reject accordingly.