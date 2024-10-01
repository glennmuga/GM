 ## Diff between Git and Github
 
 Simply put, Git is a version control system that lets you manage and keep track of your source code history. GitHub is a cloud-based hosting service that lets you manage Git repositories.
 
 If you have open-source projects that use Git, then GitHub is designed to help you better manage them. 

 ## What is the purpose of the .gitignore file?

The ‘.gitignore’ file tells Git which files and folders to ignore when tracking changes. It is used to avoid attaching unneeded files (like logs, temporary files, or compiled code) to your repository. 

This saves repository clean and targeted on important files only

## What is a version control system (VCS)?

A version control system (VCS) records the work of developers coordinating on projects. It keeps the history of code changes, permitting developers to add new code, fix bugs, and run tests securely. 

If required, they can restore a past working version, verifying project security.

## What does git clone do?
The ‘git clone’ forms a copy of a remote repository upon your local machine. It downloads all files, branches, and history, enabling you to start working on the project or contribute to it.

With git clone -b , you can download and work on an individual branch of a repository.

## What is git add?

The ‘git add‘ command marks changes in your project for the next commit. It tells Git which files to involve in the later update, making them ready to be saved in the repository.

## What is git status?
The ‘git status’ command shows the recent status of your Git repository.

It tells you which files have changed, which ones are ready to be committed, and which ones are new and unobserved. 

## What is the purpose of the git clean command?
The ‘git clean’ command is used to erase ignored files from the working directory of Git repository.

Its motive is to clean up the workspace by deleting files that are not being saved by Git, checking a clean state with only observed files present.

## What is `git checkout`?
‘git checkout‘ helps you switch between branches or return files to a previous state in Git. Now, it is suggested to use ‘git switch’ for changing branches and ‘git restore’ to return files. 

These commands are more intent on their particular tasks for better clearness and capability.

## What is ‘bare repository’ in Git?
A bare repository in Git is one missing a working directory.

It only contains version control data, making it ideal for sharing and collaboration without changing files directly.

## Explain `git rebase` and when you would use each?
‘git rebase’ moves commits from one branch to another, making a straight, linear history. Use rebase to enhance and clean up the commit history before merging

## How do you add a file to the staging area?
Use `git add <file_name>` to add a file to the staging area, forming it ready for a commit.

## What language is used in GIT?
Git is mainly developed using the C programming language. The core features and commands of Git, containing its data structures and algorithms, are applied in C.

## What is git stash?
Git stash is Git command used to temporarily store changes in your working directory that are not yet ready to be committed. 

It permits developers to conserve modifications without committing them to the repository.

## What differentiates between the commands git remote and git clone?
‘git clone’ : Downloads a full copy of a remote repository to your local computer, involving all files and history.

‘git remote’ : Controls connections to remote repositories. It sets up links to remote repositories but doesn’t download any files.

## Github actions?

GitHub Actions is a continuous integration and continuous delivery (CI/CD) platform that allows you to automate your build, test, and deployment pipeline.

You can create workflows that build and test every pull request to your repository, or deploy merged pull requests to production.

##
