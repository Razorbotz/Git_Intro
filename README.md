# Razorbotz Git Intro

Welcome to the Razorbotz Project.  This page is intended to serve as an introduction to Github for new users.  If you encounter any links that are outdated or any commands that don't work, please contact me at andrewburroughs17@gmail.com.  

## Introduction

To begin with the project, navigate to the folder you want to create the project in.  After navigating to the project folder, run the following command to download the project.  

TODO: Difference between clone and pull
TODO: Something about fetch
TODO: Take pictures of the code being executed

```
git clone https://github.com/Razorbotz/Test.git
```

After downloading the project navigate to the project folder.

```
cd Test\
```

To see what branches are currently active in the repository, execute the git branch command.

```
git branch
```

After running the command, the branches that are in the repository.  The default branch for the Test repository is the master branch.  The master branch is push protected, so you will not be able to modify any of the files in it without approval.  To modify files without overwriting anyone else's work or atttempting to push to the master branch, you will create a new local branch.  To create a local branch, run the following command and replace yourName with your name.

```
git branch yourName
```

To make sure that the branch has been created successfully, run the git branch command again.  You should see the branches that were there previously and a new one that has your name.  If that branch does not appear, run the previous command again.

```
git branch
```

To switch to your branch, run the following command.

```
git switch yourName
```

After switching to your branch, modify the files as needed.  For the purpose of this introduction, open Names.txt.  Add your name to the end of the file and save the file.  To add modified files to the repository, run the git add command.  To add all modified files, use the . option.

```
git add .
```

To specify files to add to the repository, specify the locations of the files after git add.  

```
git add \path\to\modified\file1 \path\to\modified\file2
```

TODO: git status

After adding the files to the repository, the files must be committed to the repository.  The -m flag allows the user to create a commit message that describes the changes that are being included in the commit.  

```
git commit -m "Commit message"
```

After commiting the changes to the repository, they are still staged locally and not tracked on the remote repository.  To push the changes to the remote repository, use the git push command.  The push command has the following syntax.

```
git push [repo] [branch]
```

Because the upstream branch has not been created yet, the -u flag must be used.  This will create the branch on the remote repository and push the changes to the files to that branch.

```
git push -u origin yourName
```

After pushing the changes to the repository, it will be a commit ahead of the master branch.  To move the changes to the master branch, initiate a pull request for your branch to the master.  This will require administrator authorization to merge the changes with the master branch.

To read more about git, please refer to the [git documentation](https://git-scm.com/docs).