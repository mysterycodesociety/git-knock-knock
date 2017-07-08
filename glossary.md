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
