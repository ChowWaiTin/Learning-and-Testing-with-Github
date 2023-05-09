## Summary
1. A and B working on the same branch
2. A updated file activities.txt
3. B thought that it activities.txt was unnecessary and decided to transfer the info to itinerary.txt. B subsequently deleted the file
4. A pushed the new changes
5. B pulled the new changes
6. Conflict. B resolved conflict by shifting the changes to itinerary.txt and committed the changes

## Storyline
1. Developer A and B continues to work on the itinerary. Both of them worked within the itinerary/activities branch. Developer A found a number of interesting activities and stored them in the activities.txt file

2. Meanwhile, Developer B found that it was better to place the information on the activities together with the itinerary plan in the itinerary.txt file. After some discussion with the team, he began the process of transferring the information and deleted the activities.txt file. This change was not made aware to Developer A.

3. After completing the update on the activities.txt file, Developer A staged his changes, made a commit and pushed the changes to the remote repository

4. At the same time, Developer B completed the transfer of the information and deleted activities.txt file. He staged his changes and made a commit. Before pushing his changes to the remote repository, he updated his local repository and found a conflict.
    - The file he deleted had changes

5. Developer B subsequently moved the additional information to the itinerary.txt file and made a commit

6. Developer B pushed his changes to the remote repository and proceed to inform Developer A of this change.

## Lesson Learn
1. Potential conflicts from file deletion and how to handle it.