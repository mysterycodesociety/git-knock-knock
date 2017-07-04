# Git Knock Knock

## Introduction
You will be practicing git and git branching today.

Git is a powerful tool to keep track of changes to your files over time.  You can go back and forth in time, and you can see what you did.

GitHub is a company that specializes in storing git repositories in the cloud and allowing people to share them.

Git branches are a way to protect your code while you are working on features.  Until your code is ready, your changes can be in a branch so that it doesn't break master code, which might be actively used in production.  It also allows multiple people to work on code at the same time, each on their own branch.

<img src="./assets/git-branches.png" style="width:400px;">*
 

## Game

Git Knock Knock is designed to give you practice in using basic git commands and branches.  

You will be using git to tell knock knock jokes to each other.  Until your partner has merged their changes into master, pushed it up to GitHub, and you have pulled the changes down, you will not see the next line of the joke.

1. Form a pair.
1. Your partner should be in another room.  Use slack to communicate.
1. Each person will choose one knock knock joke.
1. Decide which partner tells the joke first.
1. One person forks the repository and adds the other player as a collaborator. (Go to settings, the Collaborator tab, and search by username)
1. Both people clone the repo in Cloud 9.

Now that set up is done, each person will tell their joke to their partner, line by line.  When it is your turn, follow these steps.

1. Pull the master branch down from GitHub to get any changes your partner made.
1. Cut a new branch (use a different name every time).
1. If you are writing the first line of the joke, create a new file.
1. Add the next line of the joke.
1. Save the file.
1. Add your changes to staging.
1. Commit the change.
1. Pull master down from GitHub again (a precaution - in case it changed).
1. Merge your branch with master.
1. Checkout the master branch.
1. Merge master with your branch.
1. Push master up to GitHub.
1. Tell your partner, "You're it!  Now it's your turn to add a line."


Each person should have a knock knock joke to tell.  Start with one player's knock knock joke.  Then switch.

## Example Workflow

1. One person should fork this repository.
    1. Log on to GitHub, find this repository and click the `Fork` button to create a copy to your own account.
    1. Add the other person as a collaborartor .  Go to the Settings section of the repo, find the Collaborator section, and search for them by GitHub username or email.

1. Clone the repository.
    1. In GitHub on the repository you will share, click the `Clone or download` button and copy the SSH address for the repository (should start with git@github.com).
    1. Log into Cloud 9.
    1. In terminal in Cloud 9 (make sure you are in the root/outermost folder), type `git ` and paste in what you copied from GitHub.  Hit Enter.  Stuff will happen.

   `git clone git@github.com:username/some_repository_name.git`

1. Change your directory into the repository you just cloned.

   `cd git-knock-knock`

1. Create and checkout a branch.  (Instead of `my-branch`, give your branch a name you will remember.)

   `git checkout -b my-branch`

1. Make a change and save it.

1. Add the changed files to staging.  (ie - say, 'yes, those are changes I mean to save')

   `git add .`

1. Commit the change and add a commit message.

   `git commit -m "Made my first change"`

1. Repeat steps 5-7 until your file looks good and your code is tested.

1. Pull down changes from GitHub in case someone on your team has made changes since you started working.

   `git pull origin master`

1. Merge your branch with the master branch. (Instead of `my-branch`, use the name of your branch.)

   `git merge my-branch master`

1. Checkout the master branch.

   `git checkout master`

1. Merge master with your branch to close your branch.

   `git merge master my-branch`

1. Push your changes back to GitHub so that others can see them.

```
  git push origin master
  git push origin my-branch
```



# Glossary

## Unix Terminal Glossary

- cd (change directory)

  `cd myblog` to go into the myblog folder

- ls (list your files)

  `ls` to see a list of all files in the current directory/folder

- ./ (current directory)

  `ls ./` would list all files in the current directory/folder

- ../ (parent of current directory)

  `cd ../` would change your directory to the parent of your current directory

- ../../ (grandparent of current directory)

  `cd ../../` would change your directory to the grandparent of your current directory

- / (root directory)

  `cd /` would change your directory to the grandparent of your current directory

- ~ (home directory)


## Git Glossary

The commands you will learn today are:


 - git clone

  `git clone git@github.com:username/some_repository_name.git`

  Clone a repository.  This command allows you to copy a repository that you already have on GitHub and work with a copy locally.


 - git status

  `git status`

  This command allows you to see the status of your local files and whether they have changed or are staged for a commit.


 - git add

   `git add .` or `git add file.js`

   Add to staging.  This command will allow you to stage the changes to all files, so that they are _ready_ to commit.  It will not commit any files.


 - git commit

  `git commit -m "Centers heading 1 text"`

  Commit a change.  This command will _commit_ the changes you have made.  It will create a _commit message_ that says 'Centers heading 1 text', so that people can see what you were doing.  


 - git checkout

   `git checkout -b new-branch` to create a new branch or `git checkout new-branch` if it already exists.

   Checkout a branch.  Master is the default branch.  But you should create and work on new branches, so that you don't inject code that is not tested into Master for other people.  Each person works on a branch.  Then you merge your branch into master when your code is tested and ready.


 - git pull

   `git pull origin branch_name`

  Pull down from GitHub.  Before you do a merge, you should pull down changes from GitHub to make sure you aren't missing any changes.  You must _pull_ before you _push_.


 - git merge (two branches together)

  `git merge new-branch master` when you are merging master _into_ your branch (new-branch is checked out).
  `git merge master new-branch` when you are _closing_ your branch (master is checked out).

  Merge two branches together. To completely merge your branch into master, you must merge twice.


 - git push

  `git push origin branch_name`

  Push to GitHub.  After you have made your changes, you want to push them up to GitHub.


*Photocredit: [Atlassian](https://www.atlassian.com/git/tutorials/comparing-workflows)
