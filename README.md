# IntroductionGitEndava
This is for a class of GIT in ENDAVA internship

The next text is the solution of the content proposed in next page [Learning Git](https://learngitbranching.js.org/).

And next, I put the commands and a short explanation of them:

# PART 1: Introduction Sequence 
## EXCERCISE 1: Introduction to Git Commits
### git commit
We can use commit to upload snap of changes (that git represents), from stagin area until repository area in local machine
### git commit
In this excercise we use two commits because it started in HEAD C1, and its neccesary create the commit C3

## EXCERCISE 2 Branching in Git
### git checkout -b bugFix
In this case, we use the checkout -b, this command is a mix between "git branch bugFix" and "git checkout bugFix", because the excercise ask that we create a branch bugFix, and switch to it

## EXCERCISE 3 Merging in Git
### git checkout -b bugFix
The same case of excercise 1.2
### git commit
But in this case, use the command of excercise 1.1 to create a snap of changes of those branch, and move it to repository
### git checkout main
Next we go to switch to the main branch with this command
### git commit
And create a new snap of changes of main, and move it to repository
### git merge bugFix
And to continue, we combine in the branch main, the branch bugFix, its important in this step, that you stay on main branch and execute "git merge ..." the other branch, because if youre in another branch, for example in bugFix, and you do the merge, it can stay in bugFix branch, and dissapear the main branch (With neccesary permisions)

## EXCERCISE 4 Rebase Introduction
### git checkout -b bugFix
1.2 excercise command (create and switch to bugFix branch)
### git commit
1.1 excercise command (Snap of changes in bugFix branch from stagin area until repository)
### git checkout main
1.3 excercise command (We switch to main branch)
### git commit
1.1 excercise command (Snap of changes in main branch from stagin area until repository)
### git checkout bugFix
1.3 excercise command (We switch to bugFix branch)
### git rebase main
With this command, we move the base of the current branch to another branch not without before create another snap, in this example, the branch bugFix create a new snap but the pointer bugFix mark the last snap of main like a father

# PART 2: Ramping Up 
## EXCERCISE 1 Detach yo' HEAD
### git checkout C4
We use git checkout before a name of snap (or ID number like we viewed in class) to put the pointer in those snap, in this case HEAD becomes the new pointer, and it's different of the pointer of the branches (Detach your HEAD)

## EXCERCISE 2 Relative Refs (^)
### git checkout bugFix^
In this case, we can do the "detach of head" with another reference: the checkout, predisposes us to move to another place, bugFix is the pointer of branch (or snap), but it isnt all, the character ^ thell us that we go to put the head in the father snap of bugFix snap (Relative references, because isn't direct refference)

## EXCERCISE 3 Relative Refs #2 (~)
### git checkout HEAD^
2.2 excercise command (Put the head in the father of snap that have the head pointer)
### git branch -f bugFix C0
We use git branch, like as we saw before, to be a pointer to a snap of the changes (commits), and we use -f to reassign a branch to a commit directly, and next of it, you put the pointer and the branch to be marked, in this case, the pointer bugFix is reassigned to C0 commit
### git branch -f main C6
In this case is the same of the last command, but the main pointer is reasigned to C6 commit (In this excercise, the page propouse another valid relative reference with "~", for example "git branch -f main HEAD~3" that move the pointer main to the great grandfather, or the father of the father of the father of HEAD pointer)

## EXCERCISE 4 Reversing Changes in Git
### git reset HEAD^
We can use git reset to reverse changes by moving a branch pointer to it's father, you can use relative references to have more presition, or do the reset to another place, for example using HEAD^ or HEAD~1
### git checkout pushed
2.2 excercise command (Switch the branch to the pushed pointer)
### git revert pushed
Having diferences with reset command, the revert command is advancer, because instead of delete commits in the commits history, this command will create a new commit that inverses the changes specified

# PART 3 Moving Work Around
## EXCERCISE 1 Cherry-pick Intro
### git cherry-pick C3 C4 C7
Cherry-pick command is very useful to copy a selected commits below the current pointer HEAD, in this example, we take the commits C3, C4 and C7 to put under main; this can be used in a project to select the besties "cherrys" of the project, and put them in the main branch

## EXCERCISE 2 Interactive Rebase Intro
### git rebase -i HEAD~4