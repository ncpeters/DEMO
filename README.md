# Getting Started in GitHub

##### WARNING: do not upload any sensitive data or information onto GitHub

#### Creating a repository

1. From your profile icon at the top right of your GitHub, you can view 'Your repositories' - click this link
2. From 'Your repositories', you can select the green 'New' button
3. From here, choose the owner, and an appropriate name
4. Also tick the box for adding a 'README file', and select a .gitignore template
5. An MIT license is also sensible for when planning to make the code publicly available
6. Finally, click the green 'Create repository' button

#### Accessing a GitHub repository locally for the first time

1.	Navigate to file space where you’d like to save your local copy (note this can’t be in a shared file space) and create a folder within which to store it – e.g. make a ‘GitHub repos’ folder in your OneDrive documents space
2.	Right click in your folder space and click 'Git Bash Here' to open the programme (terminal), relative to the file path where you have created this folder (note it may be under 'Show more options')
3.	Open the online GitHub repository you want to work in and select the green button 'Code', from here you can copy the URL for the repository
4.	Within Git Bash, _git clone_ the repository to create your local copy, using the URL you copied. it's a nice practice to include the code required for cloning within your README, as below: 

(Note: the command line does not respond well to the copy and paste keyboard shortcuts (Ctrl+C and Ctrl+V). Instead, use the options via right clicking)

```shell
git clone https://github.com/ncpeters/DEMO.git
```

5. Then, you need to tell it to 'move' into that repository you have just created: 

```shell
cd DEMO
```

(cd = Change Directory)

(You can explore further Linux commands if you'd like, but _cd_ is the main one you will need to work in Git Bash).

#### Creating your own branch to work on

You can make changes directly to the 'main' branch, however it is advisable to create a branch as this way the repository is kept tidier, and it is easier to manage and track work contributed by different individuals and to keep tabs on what the changes are for.  

1.	Create a branch on GitHub:
   
a.	Click on the current branch, in this screenshot it is ‘main’ and it will provide a dropdown to enable switching to a different branch

![image](https://github.com/ncpeters/DEMO/assets/131660276/163132fa-90b2-43b5-a9fe-db83aebc0b84)


b.	Here you can start typing the name of a new branch and it will give you the option to ‘Create branch’

i.	Note: for naming branches, a useful convention is JiraIssueID-Initials-brief_description_of_branch_purpose, e.g. NDRSA-1483-NP-summary_fields

![image](https://github.com/ncpeters/DEMO/assets/131660276/8e7cf07b-ec2c-48bf-beff-ada3feeff8ce)


2.	Ensure your local copy is up to date with the changes made to the online repository using _git pull_ – this will ‘pull’, or download, any changes from the remote to your local version

```shell
git pull
```
   
3.	Ensure you are working within this newly created branch using _git checkout name_of_branch_ to switch between branches (the name of your current branch is typically shown at the end of the prompt within the command line environment)

```shell
git checkout new branch
```

For a summary of Git commands: https://book.the-turing-way.org/reproducible-research/vcs/vcs-git-summary and https://nhsdigital.github.io/rap-community-of-practice/training_resources/git/introduction-to-git/#common-git-commands 

#### Editing and saving file changes

1.	Make any changes to files or code as you normally would
2.	At any time, within the command line, you can run _git status_ to check with state of the working directory and staging area (important note – if the remote version is ahead of your local version, i.e. someone else has made changes, this will not be flagged as Git will not be aware until you run _git pull_)

```shell
git status
```

3.	Update the online/remote branch with changes made locally:
    
a.	_git add ._ or _git add <filename>_, adds files to the staging area ready for commit (the ‘.’ Means all files are added)

```shell
git add .
```

b.	_git commit -m ‘your comment here’_ to capture a snapshot of the current staging area, ready for updating the remote repository

```shell
git commit -m 'commit message here'
```

c.	_git push_ to 'push', or upload, the changes you have made to the online repository

```shell
git push
```

4.	To check the above steps have been successful you can refresh online GitHub page at this point


#### Merging and QA
    
1.	To merge this branch with the main branch via a QA step, make pull request on the GitHub page and ensure to assign a reviewer
2.	The reviewer should QA changes as usual, then respond with comments within GitHub and / or accept the merge
3.	At the point of merge, the branch should ideally be deleted, and a new branch created for the next portion of work

Managing merge conflicts:

If there is a conflict, GitHub will flag this within the pull request.

![image](https://github.com/ncpeters/DEMO/assets/131660276/4936790a-cf61-4a98-bfdb-33cdc0f8d086)



You can manage and resolve these from directly within the pull request on GitHub, or from the command line if you prefer. 

You can decide if you want to keep only your branch's changes, keep only the other branch's changes, or make a brand new change, which may incorporate changes from both branches. Delete the conflict markers <<<<<<<, =======, >>>>>>> and make the changes you want in the final merge.

If you have more than one merge conflict in your file, scroll down to the next set of conflict markers and repeat the above to resolve your merge conflict.

![image](https://github.com/ncpeters/DEMO/assets/131660276/b6890f63-48f1-4787-8eb3-45b987449c93)



Once you've resolved all the conflicts in the file, click 'Mark as resolved'.

Once you've resolved all your merge conflicts, click 'Commit merge'. This merges the entire base branch into your head branch.


