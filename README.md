# GIT VERSION CONTROL SYSTEM

## Git Installation

> Linux Debian

    ```
        sudo apt-get install git
    ```

> Linux Fedora

    ```
        sudo yum install git
    ```

> Windows

https://git-scm.com/download/win

> Mac

https://git-scm.com/download/mac

or

    ```
        brew install git
    ```

## Git Configuration

> To verify successful Git Installation

    ```
        git --version
    ```

> To set a global username and email

    ```
        git config --global user.name preferred_name

        git config --global user.email preferred_address
    ```

> To view a list of your configuration options

    ```
        git config user.name

        git config user.email
    ```

> To get full git manual

    ```
        man git
    ```

> To short cut to specific section in the manual

    ```
        git help config
    ```

> To get a smaller list of git commands

    ```
        git help
    ```

> To initialize a new project, cd to that project folder and run

    ```
        git init
    ```

> To view the hidden git folder

    ```
        cd .git
    ```

## Github

> Link to SSH option guidance when creating new repo

https://help.github.com/articles/which-remote-url-should-i-use

## Git Project and File Stages

> The three stages of a **git project**
1. .git Directory (repository)
   - origin of the project data that is pulled down from the server
2. Working Directory
   - single copy used to check out a version of the project from origin
3. Staging Area (Index)
   - used to build up a set of changes
   - after commit, changes are added to this directory

> The three stages of a **git file**
1. Committed Stage
   - the data in the file at this stage is safely stored in the local database
   - data in the file at this stage is unmodified
2. Modified
   - when changes are made, data in this file has been modified but not committed yet
3. Staged
   - in this stage, changes made to data in a file are committed so that they can be in the next local commit snapshot

## Basic Git Commands

1. **git add 'file_name'** - this adds the given file to the staging area
2. **git add .**  - this adds all files to the staging area
3. **git commit -m "message of choice"** - this commits changes to on a given file
4. **git remote add origin "github repository"** - this adds a remote repository to a local repository
5. **git push -u origin master** - this pushes changes made in the local repository to the master branch of the remote repository
6. **git status** 
   - this aids in checking for the status of a given project
   - for shorter results, you can use **git status -s** or **git status --short**
   - the **M** returned when you use the short version stands for **Modified**, the **A** stands for **New file added to the staging area** and the **??** stands for **A new file that is untracked by git**
7. **git diff**
   - shows you what changes have been staged that are ready to be committed
   - also shows you what changes have been made but not yet staged
   - **git diff --staged** also compares the previous committed files to those in the staging area.
   - **git diff --staged --no-renames** - it returns results with duplicates removed
8. **git log**
   - used for viewing the git history
   - **git log -1** - limits the number of commits returned to 1 commit
   - **git log --oneline** - list each commit on a single line
   - git log --stat - detailed view of each commit
   - git log --patch - full details of a given commit
9. **git rm "file_name"** 
   - removes a given file from the project
   - **git rm --cached "file_name"** - keeps file in the project but calls git to stop tracking it
10. **git mv old_file_name new_file_name** - this changes the file name of an existing file
11. **git branch branch_name** - this creates a new branch
12. **git checkout -b branch_name** - this creates a new branch and moves the HEAD to point to it
13. **git checkout branch_name** - this moves the HEAD to the specified branch
14. **git stash** 
    - keeps untracked files without removing them from git
    - **git stash list** or **git stash show** - shows you a list of changes that were stashed
    - **git stash pop** - gets changes out of the stash and drops them into the working directory
15. **git merge "merge_branch"** - it incorporates changes from one branch into another branch
16. **git reset** - used to reset merged changes
    - **git reset --soft "commit_id"** - when used, the given commit is moved back into the staging area
    - **git reset --mixed "commit_id"** - this is the default. It moves changes back into the working directory
    - **git reset --hard "commit_id"** - moves changes to the trash
17. **git clone "url"** - copies the remote repository into the specified location
18. **git fetch** - get updates from remote branch to local branch
19. **git pull** - downloads changes from the remote repository and updates them in the local repository 

 

## Commit format

Visit http://chris.beams.io/posts/git-commit to view the structure of a well structured commit message

## How branches work

Visit http://git-school.github.io/visualizing-git
