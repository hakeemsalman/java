# Git

Practicising from Git Learning website [https://learngitbranching.js.org/](https://learngitbranching.js.org/)

## Git Commit

> $ git commit

It create a new commit and main is move to new commit

## Branch

> $ git branch newImage

New branch is created here with the name of `newImage`. Here `$ git branch <branchName>`

Here with that same commit both main and newImage branch are present

> $ git commit

If you do `git commit` the main branch is move ahead with new commit and newImage branch is stay with old commit

Oh! no, but we want to move with `newImage` not with main `branch`

So we have to use `checkout`, this is used to change branch from one to another with branch name
`$ git checkout <branchName>`

> $ git checkout newImage; git commit;

Now new commit is moved with `newImage branch`

NOTE:-  
In Git version 2.23, a new command called `git switch` was introduced to eventually replace `git checkout`, which is somewhat overloaded (it does a bunch of different things depending on the arguments). The lessons here will still use `checkout` instead of `switch` because the `switch` command is still considered experimental and the syntax may change in the future. However you can still try out the new `switch` command in this application, and also [learn more here.](https://git-scm.com/docs/git-switch)

Ok! You are all ready to get branching. Once this window closes, make a new branch named `bugFix` and switch to that branch.

By the way, here's a shortcut: if you want to create a new branch AND check it out at the same time, you can simply type `git checkout -b <yourbranchname>`.

> git checkout -b bugFix

## Merging in Git

Great! We now know how to commit and branch. Now we need to learn some kind of way of combining the work from two different branches together. This will allow us to branch off, develop a new feature, and then combine it back in.

The first method to combine work that we will examine is git `merge`. Merging in Git creates a special commit that has two unique parents. A commit with two parents essentially means "I want to include all the work from this parent over here and this one over here, and the set of all their parents."

It's easier with visuals, let's check it out in the next view.

Here we have two branches; each has one commit that's unique. This means that neither branch includes the entire set of "work" in the repository that we have done. Let's fix that with merge.

We will `merge` the branch `bugFix` into `main`.

> $ git merge bugfix

Here what's happening, commit is going to `main` and `bugfix` is not merging with `main`. So to do that, we will be using below command.

> $ git checkout bugfix; git merge main

Since `bugFix` was an ancestor of `main`, git didn't have to do any work; it simply just moved `bugFix` to the same commit `main` was attached to.




## Git Rebase

The second way of combining work between branches is rebasing. Rebasing essentially takes a set of commits, "copies" them, and plops them down somewhere else.

While this sounds confusing, the advantage of rebasing is that it can be used to make a nice linear sequence of commits. The commit log / history of the repository will be a lot cleaner if only rebasing is allowed.

![](./assets/rebase/rebase-1.png)
![](./assets/rebase/rebase-2.png)
![](./assets/rebase/rebase-3.png)
![](./assets/rebase/rebase-4.png)


## Head

First we have to talk about "HEAD". HEAD is the symbolic name for the currently checked out commit -- it's essentially what commit you're working on top of.

HEAD always points to the most recent commit which is reflected in the working tree. Most git commands which make changes to the working tree will start by changing HEAD.

Normally HEAD points to a branch name (like bugFix). When you commit, the status of bugFix is altered and this change is visible through HEAD.

Try this

> $ git checkout C1; git checkout main; git commit; git checkout c2







