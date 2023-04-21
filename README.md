# IntroductionGitEndava
This is for a class of GIT in ENDAVA internship

The next text is the solution of the content proposed in next page [Learning Git](https://learngitbranching.js.org/).

And next, I put the commands and a short explanation of them:

# PART 1: Introduction Sequence 
## EXCERCISE 1: Introduction to Git Commits
### git commit
asd
### git commit
asd

## EXCERCISE 2 Branching in Git
### git checkout -b bugFix

## EXCERCISE 3 Merging in Git
### git checkout -b bugFix
### git commit
### git checkout main
### git commit
### git merge bugFix

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