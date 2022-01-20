# Razorbotz Git Intro

Welcome to the Razorbotz Project.  This page is intended to serve as an introduction to Github for new users.  If you encounter any links that are outdated or any commands that don't work, please contact me at andrewburroughs17@gmail.com.  **For the instructions below, the expected output is shown after the commands.**

## Introduction

To begin with the project, navigate to the folder you want to create the project in.  After navigating to the project folder, run the following command to download the project.  

```
git clone https://github.com/Razorbotz/Test.git
```

![Clone results](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_1.PNG)

After downloading the project navigate to the project folder.

```
cd Test\
```

In this folder, there is one remote repository currently defined.  To see the remote repositories that are defined in this folder, execute the git remote command.  The -v flag tells git to display the url associated with each repository as well as the name.  You should see one remote repository called origin with the url https://github.com/Razorbotz/Test.git.  To read more about the git remote syntax and other examples, refer to the git documentation located [here](https://git-scm.com/docs/git-remote).

```
git remote -v
```

![Remote results](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_2.PNG)

The git clone command makes a local copy of a remote repository stored in Github.  After executing this command, there will be a copy of all the files stored locally.  To update the files locally, use the git fetch or git pull commands.  The git fetch command downloads a copy of all of the changes from the remote repository and does not apply them to your local copy.  To merge the changes with your local versions, the git merge command should be used.  The git pull command is equivalent to executing the git fetch and git merge commands.  To see this in action, run the git pull command.

```
git pull origin master
```


This will download and merge the changes from the master branch in the origin remote repository.  Because you downloaded the most recent version of the repository, there will most likely be nothing to update, so the command will return the response.


![Pull results](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_1.PNG)



To see what branches are currently active in the repository, execute the git branch command.

```
git branch
```

![Branch results](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_4.PNG)


After running the command, the branches currently in the repository are listed.  The default branch for the Test repository is the master branch.  The branch that is currently selected is displayed in green, which is currently the master branch.  The master branch is push protected, so you will not be able to modify any of the files in it without approval.  You will need to create a local branch to avoid (1) modifying someone else's work and (2) attempting to push to the master branch.  To create a local branch, run the following command and replace yourName with your name.

```
git branch yourName
```

To make sure that the branch has been created successfully, run the git branch command again.  You should see the branches that were there previously and a new one that has your name.  If that branch does not appear, run the previous command again.

```
git branch
```

![Branch results](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_5.PNG)


To switch to your branch, run the following command.

```
git switch yourName
```

![Branch results](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_6.PNG)


After switching to your branch, modify the files as needed.  For the purpose of this introduction, open Names.txt.  Add your name to the end of the file and save the file.  To add modified files to the repository, run the git add command.  To add all modified files, use the . option.

```
git add .
```

To specify files to add to the repository, specify the locations of the files after git add.  

```
git add \path\to\modified\file1 \path\to\modified\file2
```

To view which files have been added to the repository, run the git status command.

```
git status
```

![Branch results](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_13.PNG)

After adding the files to the repository, the files must be committed to the repository.  The -m flag allows the user to create a commit message that describes the changes that are being included in the commit.  

```
git commit -m "Commit message"
```

![Commit results](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_7.PNG)


After commiting the changes to the repository, they are still staged locally and not tracked on the remote repository.  To push the changes to the remote repository, use the git push command.  The push command has the following syntax.

```
git push [repo] [branch]
```

Because the upstream branch has not been created yet, the -u flag must be used.  This will create the branch on the remote repository and push the changes to the files to that branch.

```
git push -u origin yourName
```

![Push results](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_8.PNG)


After pushing the changes to the repository, it will be a commit ahead of the master branch.  To move the changes to the master branch, initiate a pull request for your branch to the master.  To initiate a pull request, go to the [Razorbotz/Test](https://github.com/Razorbotz/Test.git) repository on Github.  Click on the master branch and select your branch from the dropdown menu.  

![Branch select](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_12.PNG)

After navigating to your branch, press the Compare & pull request button.  

![Branch results](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_9.PNG)


Add a message and comment to the pull request as necessary.  After adding all details as needed, press the Create pull request button.

![Pull request](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_10.PNG)

After submitting the pull request, a screen will pull up with an error message that the merge needs administrator approval.  This is the expected result and the merge will be approved when I am able to.

![Pull results](https://github.com/Razorbotz/Test/blob/pictures/pictures/Test_11.PNG)


To read more about git, please refer to the [git documentation](https://git-scm.com/docs).