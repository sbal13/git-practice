# Git!

## What is it?

Git is a version control system (VCS) used for saving code and managing contributions to it. It allows you to keep all previous versions of your code without having to keep around seperate copies of your code.

## How does it work?

Git uses a data structure called a linked list to connect nodes called "commits" to each other.

A commit is composed of 3 main pieces of information:
1. The name of the commit (usually a hashed value)
2. The content of the commit (the changes made during that commit)
3. Pointer(s) to the previous commit(s)


## Saving 

`git add`

Stages parts of your repository to be committed.

`git commit`

Finalizes a commit. Use `-m` flag to describe what you're committing

`.gitignore`

Used to prevent entire files from being staged for commit.

Example uses:
API keys
Database
Your diary
Log files
Schema
Anything secret or generated automatically by running application

## Reading

`git status`

Gives your information about what has and has not been staged for commit.

`git log`

Gives you a history of all of your commits.

`git diff`

Gives you the diff between the current state of your files and the last commit. Basically, anything that hasn't been committedd yet.

`git stash`




## Remote vs local

`git remote`

`git push`

`git fetch`

`git pull`

`git clone`

## Branching

`git checkout`

`git branch`

## Updating

`git merge`

`git rebase`

## Rewriting history

`git reset --hard <COMMIT HASH>`

## Forking and Pull Requests

I'm GONNA USE REBASE

NOW