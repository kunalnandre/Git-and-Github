## What Is Git?

Git is a distributed version control system (VCS) that empowers you to track changes made to project files. It streamlines code management and team collaboration. Whether you’re an individual developer or a team member, learning Git simplifies version control and enhances effectiveness.

The main benefits of **_Git_** are:
* Powerful and detailed change tracking, which means less conflicts.
* The job can be done offline - except when you are receiving/sending changes to the server.
* Workflow is flexible.
* Branching and merging is more reliable.
* It is very fast.

## Understanding the Git Workflow:

A Git project consists of three major sections: **the working directory, the staging area, and the git directory.**

The working directory is where you add, delete, and edit files. Then, the changes are indexed in the staging area. After you commit your modifications, a snapshot of the changes will be saved in the directory.

After Installation We need To configure git using git bash
```shell
git config --global user.name 'YourName'
```
```shell
git config --global user.email 'YourEmail'
```

## Most Commonly Used Git Commands:

1. This command initiates a new Git repository within a directory. Here’s the basic git init usage

```shell
git init
```
2. To create a new repository while specifying the project’s name, use the following command:
```shell
git init [project name]
```
3. This command is used to stage file changes, preparing them for the next commit:
```shell
git add file1.txt
```
4. Use this command to create a commit message for the changes, making them part of your project’s history:
```shell
git commit -m "Add new feature"
```
5. This command displays valuable insights into your files’ modifications and staging status.
```shell
git status
```
6. The basic git log usage It lets you view a chronological list of commit history: 
```shell
git log
```
7. This command lets you compare changes between your working directory and the most recent commit. For example, this git diff usage identifies the differences in a specific file:
```shell
git diff file1.txt
```
8. To compare changes between two commits, use the following:
```shell
git diff commit1 commit2
```
9. This command removes files from your working directory and stages the removal for the next commit.
```shell
git rm file1.txt
```
10. Use this command to rename and move files within your working directory. Here’s the Git command to rename a file:
```shell
git mv file1.txt file2.txt
```
11. To move a file to a different directory, enter:
```shell
git mv file1.txt new_directory/
```
## Git Remote Repository Commands:
1. This command creates a copy of a remote repository on your local machine. A basic git clone usage is to clone a repository from GitHub:
```shell
git clone https://github.com/username/my-project.git
```
2. This command sends your local Git branch commits to a remote repository, updating it with your latest changes.

For example, you want to push changes from the local repository called “main” to the remote repository named “origin”:
```shell
git push origin main
```
3. This command fetches and integrates changes from a remote repository into your current local branch. Here’s a git pull usage example to pull changes from the master branch:
```shell
git pull origin master
```
4. To retrieve new commits from a remote repository without automatically merging them into your current branch, use this command:
```shell
git fetch origin
```
5. This command manages remote repositories associated with your local repository. The basic git remote usage lists the remote repository:
```shell
git remote
```
6. To add a new remote repository, specify its name and URL. For example:
```shell
git remote add origin https://github.com/username/origin.git
```
## Git Branch
A Git branch is like a copy of your project where you can work on new stuff without messing up the original. When you're done, you can merge the changes back in.

1. In any Git project we can view all branches by entering the following command in the command line:
```shell
git branch
```
2. If there is no branch created, there will be no output in the terminal. Creating a branch is really simple:
```shell
git branch [new_branch]
```
3. Then, we need to move to the newly created development branch. To do this, we will run the following command:
```shell
git checkout [new_branch]
```
4. The output will inform us that we switched to a new branch. We called it test, so:
```shell
Switched to branch ‘test’
```
Now, in that new development branch, we can create as many code modifications as we want without having to change anything in the main one. As we can see, it keeps the program organized for new code inclusions.

5. If we run the command to list the branches again, we will see that a new branch is added and that we are located in it.
```shell
git branch
```
There is something we need to keep in mind if we want to make a new development branch. First, we need to commit to the main branch for Git to understand what the master branch is. If we do not do this, we will get an error. So first, commit and then create the development branches.

6. If we want to remove a branch from Git, we can do it with the following command:
```shell
git branch -d [branch_name]
```
However, in order to do this, we must not be located on the branch we want to remove. So in this case, we move to the master branch and from there delete the branch we just created:
```shell
git checkout master
```
```shell
git branch -d test
```
Finally, there comes a point where we have made many modifications to a development branch. And it becomes stable, so we want to link it to another development branch. For that, there is the merge command.

First, locate the development branch to which the second branch is to be attached. For example, we will attach the test branch to the master branch. Then, we have to place ourselves in the master branch and merge with the command:
```shell
git merge [branch]
```
As you can see the basic Git branch functions are pretty easy. You just need to know the fundamentals, and try to keep your management clean.

## Git Stash 
Git Stash is a command in the Git version control system that allows you to temporarily save changes in your working directory that you do not want to commit immediately but also do not want to discard.

1. If you want to save your local changes in the backstage that shouldnt be  committed. This command will take all the changes in your working directory , You run this command
```shell
git stash 
```
After running git stash, your working directory will be reverted to the state of the last commit. This means your changes are no longer present in your working directory.

2. When you're ready to bring back your stashed changes, you can use these two commands :
```shell
git stash apply 
```
*git stash apply will apply the most recent stash and keep it in the stash stack*
```shell
git stash pop
```
*git stash pop will apply the most recent stash and remove it from the stash stack*

3. You can stash multiple sets of changes, and they will be stored in a stack , you can  specify which stash you want to apply or pop if you have more than one by using this command:
```shell
git stash list
```

4. You can remove stashed changes from the stack using these commands:
```shell
git stash drop
or
git stash clear // for clearnig all stashes
```

Here are some common use cases for **_git stash_**:

* Switching branches: When you want to switch to a different branch but have unfinished work in your current branch.
*  Pulling in changes: Before pulling changes from a remote repository to avoid conflicts.
*  Temporary experimentation: When you want to try something out without committing your changes.
*  Switching focus: When you need to focus on a different task and want to save your current work.

 _git it stash is a valuable tool for managing your work in Git and maintaining a clean and organized version control history_
 
#### So, apply this knowledge and continue refining your Git commands skill. Good luck!
