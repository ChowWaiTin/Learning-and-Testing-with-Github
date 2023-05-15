## Summary
1. A and B working on the same branch
2. A updated file activities.txt
3. B thought that it activities.txt was unnecessary and decided to transfer the info to itinerary.txt. B subsequently deleted the file
4. A pushed the new changes
5. B pulled the new changes
6. Conflict. B resolved conflict by shifting the changes to itinerary.txt and committed the changes

## Storyline
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
        Visit National Park - Can be added to day 1
        Visit Museum - Can be added to day 2
        Shopping at A Mall - Can be added to day 2
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