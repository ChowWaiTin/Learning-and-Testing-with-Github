# Learning Git with Real-Life Applications

## Context of Real-Life Application
A group of developers decided to go on vacation trip together after their recent project has been deployed and commisioned. The lead developer of the developement team decided to use GitHub to store the details of their vacation trip such as the itenary, budget planning and etc. By using GitHub, this would also allow the lead developer to be able to track any changes made effortlessly in the planning of the trip by the whole team.

## 1. Setting up the Pre-requisites
Before the team of developers can plan for their trip, the lead developer would need to ensure that the team would have the following things required:

- Having [Git Installed](./1.%20Setting%20up%20the%20Pre-requisites/Download%20and%20Install%20Git%20Bash.md) on their Local Device
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

After having initialized the repository for the project, the team can start to collaborate for the planning of the trip together. But before they begin, the team member would need to have a local copy of the remote repository on their local device. To do so, the lead developer teaches the team how to clone the remote repository onto their local device

For the steps on how to clone the global repository and find out more, [click here](./3.%20Clone%20Repo%20To%20Start%20Collaborating//8._Clone_Repo.md)! 

## 4. Planning for the Trip - Collaboration

After the cloning of the remote repository is done, the team members can proceed on to collaborate in the planning of the trip. 

 - Throughout this collaboration, Visual Studio Code will be used for the editing of document. 
    [Set up Visual Studio code](./1.%20Setting%20up%20the%20Pre-requisites/Download%20and%20Install%20Visual%20Studio%20Code.md)

To be able to contribute individually to the planning of the trip, the lead developer taught his team on the following topics below:

1. The *basics and importance of branching*  and *following a branching strategy (i.e. feature branching model)* which will allow the team to plan the trip in parallel.
2. The importance of *code synchronization* so that their local repository is always up-to-date with any latest changes in the remote repository.
3. How to *manage local their changes* and *push them to their feature branches in the remote repository*.
4. *Merging/Integrating the changes* made in their feature branch back to the common branch in their remote repository.

After this has been taught, each of the team members begin applying what they have learnt during the collaboration. Along the journey of their collaboration to plan for an epic vacation trip, they encountered many life's precious lessons for a software developer when using GitHub.

Click on anyone of the storyline below to learn what they have reflected!!!

* [*Storyline 1*](./4.%20Collaboration%20as%20A%20Team/1._Contributing_Individually.md)

    This storyline is about Developer A working individually on the tasks he was given which is plan for the Day 1 itinerary of the trip. In this storyline, you will be able to learn how Developer A was able to apply what he has learnt on the topics taught by the lead developer.

* [*Storyline 2*](./4.%20Collaboration%20as%20A%20Team/2._Working_On_The_Same_Branch.md)

    As Developer A continues to plan for the Day 1 itinerary of the trip, he begins to have difficulty on choosing between 2 places for sightseeing on the trip. On noticing this, Developer B decides to help out Developer A by working on the same feature branch that Developer A created. In this storyline, you will be able to learn the issues/struggles that both Developer A and B faced when working together and making changes on the same feature branch.

* [*Storyline 3*](./4.%20Collaboration%20as%20A%20Team/3._Editing%26Deleting_The_%20Same_File.md)

    As the team continues to collaborate together, both Developer A and B continue to working together on the same feature branch created by Developer A. In this collaboration between Developer A and B, they are both working on the planning of the activities to do for the trip. 
    
    While working together, Developer A created a new file (i.e. activity.txt) for the repository to store information related to all the activities for the trip.
    However, with a different perspective, Developer B felt that information related to activities for the trip should be stored in the individual file related to each itinerary of the day (i.e. day1_itinerary.txt, day2_itinerary.txt, day3_itinerary.txt, day4_itinerary.txt).

    Thus, Developer B decided to split the information stored in the activity.txt and transfer them to the respective itinerary files (i.e. day1_itinerary.txt, day2_itinerary.txt, day3_itinerary.txt, day4_itinerary.txt). And then deleting the activity.txt file from the repository.

    Because of the lack of communication between both Developers A and B, they encountered errors/conflicts while merging the changes they have made to the remote repository.

    [Click here](./4.%20Collaboration%20as%20A%20Team/3._Editing%26Deleting_The_%20Same_File.md) to find out how they resolved and learnt from this issue.

* [*Storyline 4*](./4.%20Collaboration%20as%20A%20Team/4._Merging_Different_Branches.md)

    As collaboration continues, both Developer A and B continue to working together on the same feature branch created by Developer A. This time round, they begin working on the planning for their food by listing the different food outlets available. 
    
    While working together, Developer A created a new file (i.e. activity.txt) for the repository to store information related to all the activities for the trip.
    However, with a different perspective, Developer B felt that information related to activities for the trip should be stored in the individual file related to each itinerary of the day (i.e. day1_itinerary.txt, day2_itinerary.txt, day3_itinerary.txt, day4_itinerary.txt).

    Thus, Developer B decided to split the information stored in the activity.txt and transfer them to the respective itinerary files (i.e. day1_itinerary.txt, day2_itinerary.txt, day3_itinerary.txt, day4_itinerary.txt). And then deleting the activity.txt file from the repository.

    Because of the lack of communication between both Developers A and B, they encountered errors/conflicts while merging the changes they have made to the remote repository.

    [Click here](./4.%20Collaboration%20as%20A%20Team/3._Editing%26Deleting_The_%20Same_File.md) to find out how they resolved and learnt from this issue.

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