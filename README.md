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

Temporarily stashes any changes since previous commit and saves it to the stash list. Use `git stash list` to see list of all stashes (stored in reverse order, i.e. 0 is the latest stash). `git stash apply` to apply all stashed changes to code, `git stash apply <stash identifier>` to apply a specific stash.


## Remote vs local

`git remote`

Shows the remotes attachedd to this repo. Adding `-v` flag gives information about which online repo the remote is pointing to. Adding `add <name> <ssh>` allows you to add more remotes to this repo. 

`git push`

Move commit history from local machine to remote repository

`git fetch`

Get a branch from a remote that you do not have saved locally on your machine.

`git pull`

Short for `git fetch && git merge`. First fetches branch from remote repo and then merges into whatever branch you are on.

`git clone`

"Clones" repo onto local machine. Downloads the code.

## Branching

`git branch`

Thread onto which you can add your work without interrupting or changing other "threads."

`git checkout`


## Updating

`git merge`

`git rebase`

## Rewriting history

`git reset --hard <COMMIT HASH>`

## Forking and Pull Requests

THIS IS MASTER

ANOTHER THING ON MASTER