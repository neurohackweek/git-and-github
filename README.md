# Git and Github 1 & 2

#### Neurohackweek 2016 @ University of Washington  
#### Led by Bernease Herman
#### Data Scientist at UW eScience Institute  

## Agenda

### First Hour  (Git and Github 1)

1. Introduction (2 min)
1. Survey of participant prior knowledge (2 min)
1. Setup Git and Github accounts (10 min)
1. Git review, or *fast* intro (15 min)
1. Github remotes and collaboration (10 min)
1. Merge conflicts (10 min)

### Second Hour  (Git and Github 2)

1. [Re-]Introduction (2 min)
1. *Extremely fast* review of last hour (3 min)
1. Reset, checkout, revert (7 min)
1. Github forks and pull requests (15 min)
1. Branches (8 min)
1. Collaboration workflows (5 min)
1. Rebasing vs. Merging (10 min)
1. HEAD, refs, and detached HEAD (5 min, if time)

## Git and Github 1

### Introduction

#### Who am I?

#### Why version control?

### Survey of participant prior knowledge

Show of hands, who is comfortable with the following:

** Command line: **   
 * changing directories and making folders
 * terminal text editor (e.g., nano, vim, emacs)

** Git: **  
 * git add, git commit
 * git push, pull
 * merge conflicts
 * branches
 * rebasing

** Github: **  
 * pull requests
 * forking a repo

### Setup Git and Github accounts

#### Check for Git on Windows

#### Check for Git on Mac or Linux

To check if installed, go to terminal and type the following.

    git --version

If you see any version number, you should be fine for the two sessions.

#### Set config settings for Git

We'll follow Software Carpentry lesson on setting up:
http://swcarpentry.github.io/git-novice/02-setup/

In short, type the following in your terminal (excluding `$`):

    $  git config --global user.name "Vlad Dracula"
    $  git config --global user.email "vlad@tran.sylvan.ia"
    $  git config --global color.ui "auto"
	$  git config --global core.editor "nano -w"  #for nano users

#### Sign up for Github

Go to https://github.com/join and follow instructions. Free version is fine for now, but there is a process to get private repositories with an .edu email address.

### Git review, or *fast* intro

We'll follow a few lessons in the Software Carpentry lesson, albeit very quickly.

#### Creating a repository

Resource: http://swcarpentry.github.io/git-novice/03-create/

Create and move to the folder in which we wish to hold our project (using `cd` and `mkdir`). Type following into terminal:

    $  git init

This will create an empty repository.

#### Tracking changes

Resource: http://swcarpentry.github.io/git-novice/04-changes/

`git status` shows the status of a repository.

`git add` puts files in the staging area.

`git commit` saves the staged content as a new commit in the local repository.

#### Exploring history

Resource: http://swcarpentry.github.io/git-novice/05-history/

`git diff` displays differences between commits.

`git checkout` recovers old versions of files.

#### Ignoring things

Resource: http://swcarpentry.github.io/git-novice/06-ignore/

The `.gitignore` file tells Git what files to ignore.

### Github remotes and collaboration

#### Remotes in Github

Resource: http://swcarpentry.github.io/git-novice/07-github/

A local Git repository can be connected to one or more remote repositories.

Use the HTTPS protocol to connect to remote repositories until you have learned how to set up SSH.

`git push` copies changes from a local repository to a remote repository.

`git pull` copies changes from a remote repository to a local repository.

#### Collaborating

Resource: http://swcarpentry.github.io/git-novice/08-collab/

`git clone` copies a remote repository to create a local repository with a remote called origin automatically set up.

### Merge conflicts

Resource: http://swcarpentry.github.io/git-novice/09-conflict/

Conflicts occur when two or more people change the same file(s) at the same time.

The version control system does not allow people to overwrite each other’s changes blindly, but highlights conflicts so that they can be resolved.

## Git and Github 2

### *Extremely fast* review of last hour (3 min)

See **Git review, or *fast* intro** above.

### Reset, Checkout, Revert (7 min)

Resource: https://www.atlassian.com/git/tutorials/resetting-checking-out-and-reverting

### Github forks and pull requests (15 min)

#### Forking the `neurohackweek/git-and-github` repo

https://www.github.com/neurohackweek/git-and-github

This will create a new repository for your Github user, `<your-username>/git-and-github`. You will make changes on your local, push to this repository, then pull requests to upstream.

Git docs on forking: https://help.github.com/articles/fork-a-repo/

#### Sync upstream (`neurohackweek/git-and-github`)

Further down on same page of Git docs on forking: https://help.github.com/articles/fork-a-repo/#step-3-configure-git-to-sync-your-fork-with-the-original-spoon-knife-repository

#### Add file and make changes

Inside the repository, there is a participant folder. I'd like you to create a .txt file inside that folder named `<first>-<last>.txt`.

The file should contain a sentence on your Git/Github or other version control experience along with any questions you have.

##### Example
###### git-and-github/participants/bernease-herman.txt

    I've used Git as an individual, but haven't used remote repositories or collaborative features like pull requests.

	I'd like to know how I can lookup the people who've changed a particular file in my repo.

### Branches (8 min)

So far, we've only worked on the `master` branch. Branches are a great way to organize experimental features or those that may occur non-linearly.

Resource: https://www.atlassian.com/git/tutorials/using-branches

### Collaboration workflows (5 min)

So far, we've experimented with two workflows for collaboration. In the first hour, we added a collaborator to the same central repository and pushed changes directly there. Recently, we forked a repository into our personal Github accounts then submitted pull requests to the maintainer.

These two are very popular workflows, as they can use but don't require branches. Our new knowledge of branches opens us up to other workflows.

Resource: https://www.atlassian.com/git/tutorials/comparing-workflows

### Rebasing vs. Merging (10 min)

Merging is a safe way of combining two branches, but not necessarily clean. The Git log will have an additional commit for every merge.

Rebasing allows us to replay commits at the end of a branch. This can make the tree linear and cleaner, but at the risk of losing changes.

Resource: https://www.atlassian.com/git/tutorials/merging-vs-rebasing
