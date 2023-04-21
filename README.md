# IntroductionGitEndava
This is for a class of GIT in ENDAVA internship

The next text is the solution of the content proposed in next page [Learning Git](https://learngitbranching.js.org/).

And next, I put the commands and a short explanation of them:

# PART 1: Introduction Sequence 
## EXCERCISE 1: Introduction to Git Commits
### git commit
We can use commit to upload pic of changes (that git represents), from stagin area until repository area in local machine
### git commit
In this excercise we use two commits because it started in HEAD C1, and its neccesary create the commit C3

## EXCERCISE 2 Branching in Git
### git checkout -b bugFix
In this case, we use the checkout -b, this command is a mix between "git branch bugFix" and "git checkout bugFix", because the excercise ask that we create a branch bugFix, and switch to it

## EXCERCISE 3 Merging in Git
### git checkout -b bugFix
The same case of excercise 1.2
### git commit
But in this case, use the command of excercise 1.1 to create a pic of changes of those branch, and move it to repository
### git checkout main
Next we go to switch to the main branch with this command
### git commit
And create a new pic of changes of main, and move it to repository
### git merge bugFix
And to continue, we combine in the branch main, the branch bugFix, its important in this step, that you stay on main branch and execute "git merge ..." the other branch, because if youre in another branch, for example in bugFix, and you do the merge, it can stay in bugFix branch, and dissapear the main branch (With neccesary permisions)

## EXCERCISE 4 Rebase Introduction
### git checkout -b bugFix
### git commit
### git checkout main
### git commit
### git checkout bugFix
### git rebase main

# PART 2: Ramping Up 
## EXCERCISE 1 Detach yo' HEAD
### git checkout C4

## EXCERCISE 2 Relative Refs (^)
### git checkout bugFix^

## EXCERCISE 3 Relative Refs #2 (~)
### git checkout HEAD^
### git branch -f bugFix C0
### git branch -f main C6

## EXCERCISE 4 Reversing Changes in Git
### git reset HEAD^
### git checkout pushed
### git revert pushed

# PART 3 Moving Work Around
## EXCERCISE 1 Cherry-pick Intro
### git cherry-pick C3 C4 C7

## EXCERCISE 2 Interactive Rebase Intro
### git rebase -i HEAD~4