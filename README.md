# IntroductionGitEndava
This is for a class of GIT in ENDAVA internship.

The next text is the solution of the content proposed in next page [Learning Git](https://learngitbranching.js.org/).

And next, I put the commands and a concise explanation of them:

# PART 1: Introduction Sequence 
## EXCERCISE 1: Introduction to Git Commits
### git commit
We can use commit to upload snap of changes (that git represents), from staging area until repository area in local machine.
### git commit
In this exercise we use two commits because it started in HEAD C1, and its necessary create the commit C3.

## EXCERCISE 2 Branching in Git
### git checkout -b bugFix
In this case, we use the checkout -b, this command is a mix between "git branch bugFix" and "git checkout bugFix", because the exercise ask that we create a branch bugFix, and switch to it.

## EXCERCISE 3 Merging in Git
### git checkout -b bugFix
The same case of exercise 1.2.
### git commit
But in this case, use the command of exercise 1.1 to create a snap of changes of those branches, and move it to repository.
### git checkout main
Next, we go to switch to the main branch with this command.
### git commit
And create a new snap of changes of main and move it to repository.
### git merge bugFix
And to continue, we combine in the branch main, the branch bugFix, its important in this step, that you stay on main branch and execute "git merge ..." the other branch, because if you’re in another branch, for example in bugFix, and you do the merge, it can stay in bugFix branch, and disappear the main branch (With necessary permissions).

## EXCERCISE 4 Rebase Introduction
### git checkout -b bugFix
1.2 exercise command (create and switch to bugFix branch).
### git commit
1.1 exercise command (Snap of changes in bugFix branch from staging area until repository).
### git checkout main
1.3 exercise command (We switch to main branch).
### git commit
1.1 exercise command (Snap of changes in main branch from staging area until repository).
### git checkout bugFix
1.3 exercise command (We switch to bugFix branch).
### git rebase main
With this command, we move the base of the current branch to another branch not without before creating another snap, in this example, the branch bugFix create a new snap but the pointer bugFix mark the last snap of main like a father.

# PART 2: Ramping Up 
## EXCERCISE 1 Detach yo' HEAD
### git checkout C4
We use git checkout before a name of snap (or ID number like we viewed in class) to put the pointer in those snap, in this case HEAD becomes the new pointer, and it's different of the pointer of the branches (Detach your HEAD).

## EXCERCISE 2 Relative Refs (^)
### git checkout bugFix^
In this case, we can do the "detach of head" with another reference: the checkout, predisposes us to move to another place, bugFix is the pointer of branch (or snap), but it isn’t all, the character ^ tell us that we go to put the head in the father snap of bugFix snap (Relative references, because isn't direct reference).

## EXCERCISE 3 Relative Refs #2 (~)
### git checkout HEAD^
2.2 exercise command (Put the head in the father of snap that have the head pointer).
### git branch -f bugFix C0
We use git branch, like as we saw before, to be a pointer to a snap of the changes (commits), and we use -f to reassign a branch to a commit directly, and next of it, you put the pointer and the branch to be marked, in this case, the pointer bugFix is reassigned to C0 commit.
### git branch -f main C6
In this case is the same of the last command, but the main pointer is reassigned to C6 commit (In this exercise, the page propose another valid relative reference with "~", for example "git branch -f main HEAD~3" that move the pointer main to the great grandfather, or the father of the father of the father of HEAD pointer).

## EXCERCISE 4 Reversing Changes in Git
### git reset HEAD^
We can use git reset to reverse changes by moving a branch pointer to its father, you can use relative references to have more precision, or do the reset to another place, for example using HEAD^ or HEAD~1.
### git checkout pushed
2.2 exercise command (Switch the branch to the pushed pointer).
### git revert pushed
Having differences with reset command, the revert command is advancer, because instead of deleting commits in the commit’s history, this command will create a new commit that inverses the changes specified.

# PART 3 Moving Work Around
## EXCERCISE 1 Cherry-pick Intro
### git cherry-pick C3 C4 C7
Cherry-pick command is extremely useful to copy a selected commits below the current pointer HEAD, in this example, we take the commits C3, C4 and C7 to put under main; this can be used in a project to select the besties "cherrys" of the project and put them in the main branch.

## EXCERCISE 2 Interactive Rebase Intro
### git rebase -i HEAD~4
Like the context of the page say, cherry-pick is great when you know which commits you want, but don't cover the cases where you don't know what commits you want. In this case, we go to use the command rebase, but with the -i option, with this option, git will open a window to show which commits you want to put under the pointer of the rebase, in this window you can reorder and select or unselect the commits to copy under the pointer.
In this exercise, we need to put C3, C5 and C4 commits under the overHere pointer, but we know that it's located four commits up, or before to the current commit, for this reason we can put "git rebase -i HEAD~4", which is the same as saying "git rebase -i overHere", next, we unselect the C2 commit and put the order: C3, C5, C4. Click in Confirm button and voilà, git does the magic for you.