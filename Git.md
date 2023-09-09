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