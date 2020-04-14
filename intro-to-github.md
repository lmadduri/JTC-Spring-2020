# What is GitHub?
GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere. Think of it like Google Docs for code. 
A version control system, or VCS, tracks the history of changes as people and teams collaborate on projects together. As the project evolves, teams can run tests, fix bugs, and contribute new code with the confidence that any version can be recovered at any time. Developers can review project history to find out:

- Which changes were made?
- Who made the changes?
- When were the changes made?
- Why were changes needed?

This tutorial teaches you GitHub essentials like repositories, branches, commits, and Pull Requests. You’ll create your own Hello World repository and learn GitHub’s Pull Request workflow, a popular way to create and review code.

# Tutorial
Sign up for Github using your Columbia email address. (optional) Confirm your educational affiliation at https://education.github.com/pack to be able to access additional resources and get Github Pro.
You also need to install Git on your computer. 

## Linux
Open your command line, and use the command ```$ sudo dnf install git-all``` to download Git.

## Windows
Go to https://git-scm.com/download/win and Git will download automatically. 

## MacOS
Try running ```$ git --version``` on your Terminal app.
If you don’t have Git installed already, it will prompt you to install it.

# Basics
## What’s a repository?
A repository, or Git project, encompasses the entire collection of files and folders associated with a project, along with each file’s revision history. The file history appears as snapshots in time called commits.
To use Git, developers use specific commands to copy, create, change, and combine code. These commands can be executed directly from the command line-- also known as the Terminal on Mac systems, and Powershell on Windows.

Here are some common commands for using Git:

```git init``` initializes a brand new Git repository and begins tracking an existing directory. It adds a hidden subfolder within the existing directory that houses the internal data structure required for version control.

```git clone``` creates a local copy of a project that already exists remotely. The clone includes all the project’s files, history, and branches.

```git add``` stages a change. Git tracks changes to a developer’s codebase, but it’s necessary to stage and take a snapshot of the changes to include them in the project’s history. This command performs staging, the first part of that two-step process. Any changes that are staged will become a part of the next snapshot and a part of the project’s history. Staging and committing separately gives developers complete control over the history of their project without changing how they code and work.

```git commit``` saves the snapshot to the project history and completes the change-tracking process. In short, a commit functions like taking a photo. Anything that’s been staged with git add will become a part of the snapshot with git commit.

```git status``` shows the status of changes as untracked, modified, or staged.

```git pull``` updates the local line of development with updates from its remote counterpart. Developers use this command if a teammate has made commits to a branch on a remote, and they would like to reflect those changes in their local environment.

```git push``` updates the remote repository with any commits made locally to a branch.

# The GitHub Flow
The GitHub flow has six steps, each with distinct benefits when implemented:

- Create a branch: Topic branches created from the canonical deployment branch (usually master) allow teams to contribute to many parallel efforts. Short-lived topic branches, in particular, keep teams focused and results in quick ships.
- Add commits: Snapshots of development efforts within a branch create safe, revertible points in the project’s history.
- Open a pull request: Pull requests publicize a project’s ongoing efforts and set the tone for a transparent development process.
- Discuss and review code: Teams participate in code reviews by commenting, testing, and reviewing open pull requests. Code review is at the core of an open and participatory culture.
- Merge: Upon clicking merge, GitHub automatically performs the equivalent of a local ‘git merge’ operation. GitHub also keeps the entire branch development history on the merged pull request.
- Deploy: Teams can choose the best release cycles or incorporate continuous integration tools and operate with the assurance that code on the deployment branch has gone through a robust workflow.

# Examples

### Example: Contribute to an existing repository
The statements preceded by a # are comments, and the rest are commands that run on your computer's command line.
To run these commands, open up Terminal if you're using Mac, PowerShell if you're using Windows, and your command line if you're using Linux.
```
# download a repository on GitHub.com to our machine
git clone https://github.com/me/repo.git

# change into the `repo` directory
cd repo

# create a new branch to store any new changes
git branch my-branch

# switch to that branch (line of development)
git checkout my-branch

# make changes, for example, edit `file1.md` and `file2.md` using the text editor

# stage the changed files
git add file1.md file2.md

# take a snapshot of the staging area (anything that's been added)
git commit -m "my snapshot"

# push changes to github
git push --set-upstream origin my-branch
```


### Example: Start a new repository and publish it to GitHub

First, you will need to create a new repository on GitHub. 

```
# create a new directory, and initialize it with git-specific functions
git init my-repo

# change into the `my-repo` directory
cd my-repo

# create the first file in the project
touch README.md

# git isn't aware of the file, stage it
git add README.md

# take a snapshot of the staging area
git commit -m "add README to initial commit"

# provide the path for the repository you created on github
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git

# push changes to github
git push --set-upstream origin master
```
