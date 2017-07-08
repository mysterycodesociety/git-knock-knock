# Git merge

Most of the time, merges go just fine.

But occasionally, you and another coworker (or possibly yourself!) try to merge two changes that git doesn't know how to handle.

Typically, this happens because two people have touched the very same line of code at around the same time, and git doesn't know how to handle it.  Or two people create a file with the same name, and git doesn't know what the right name should be.

We are going to create a merge conflict and show you how to handle it.

1. Create a new branch and switch over to it.
1. Create a new file in the root called `try-to-merge.md`, with exactly that capitalization, puncutation, and spelling.
1. Add anything to the file.
1. Add and commit the change.

Now we're going to pretend that one of your collaborators created a file with the same name and is ready to merge it into master.


1. Checkout the master branch.
1. Pull down the branch `practice-merge-conflicts`.
  `git pull origin practice-merge-conflicts`
1. Checkout that branch.
1. Merge the `practice-merge-conflicts` branch with `master`.
1. Checkout `master`.
1. Merge master with the `practice-merge-conflicts` branch.


Ok.  So far so good.  We've made our change on our branch.

We've pretended we were a coworker and merged the `practice-merge-conflicts` branch with master.

Now we're going to be ourselves again and try to merge our branch into master.

1. Checkout your branch.
1. Try to merge your branch with master.

You should have a merge conflict.  In command line, you should get an error message similar to this:

```
  git-knock-knock git:(my-branch) ✗ git merge master
  Auto-merging try-to-merge.md
  CONFLICT (add/add): Merge conflict in try-to-merge.md
  Automatic merge failed; fix conflicts and then commit the result.
  git-knock-knock git:(my-branch) ✗ 
```

The message is telling you that it tried to merge and had a conflict.  Notice that you have an `✗` beside your command line indicating that there are unsaved changes in your workspace.

The file that has the merge conflict should be provided.  If more than one file is affected, you will see a line for each one.

Go to the `try-to-merge.md` file and open it.  It should look like this.


```
<<<<<<< HEAD
Something else.
=======
See if you can merge me!

Hey, looks like two people had the same idea, but they did slightly different things.  Try to fix it!
>>>>>>> practice-merge-conflicts
```

Your change and your coworker's change should be in the same file. Your change should be between `<<<<<<< HEAD` and the `=======`.  Your coworker's change should be between `=======` and `>>>>>>> practice-merge-conflicts`.

Remove those markings and decide how to edit the rest of the file.  Then save the file and close it.

Go back to command line.  Git add to save your change and git commit again.  You should now be able to continue with your merge.

1. Checkout master.
1. Merge master with your branch.
1. Push to GitHub.

Yay!  You handled your first merge conflict.