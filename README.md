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

- API keys
- Database
- Your diary
- Log files
- Schema
- Anything secret
- Anything generated automatically application (generally)

## Info

`git status`

Gives your information about what has and has not been staged for commit.

`git log`

Gives you a history of all of your commits.

`git diff`

Gives you the diff between the current state of your files and the last commit. Basically, anything that hasn't been committedd yet.

## Remote vs local

`git clone`

"Clones" repo onto local machine (i.e. downloads the code)

`git remote`

Shows the remotes attached to this repo. Adding `-v` flag gives information about which online repo the remote is pointing to. Adding `add <name> <ssh>` allows you to add more remotes to this repo. 

`git push <remote> <branch>`

Move commit history from local machine to remote repository

`git fetch <remote> <branch>`

Get a branch from a remote that you do not have saved locally on your machine.

`git pull <remote> <branch>`

Short for `git fetch && git merge`. First fetches branch from remote repo and then merges into whatever branch you are on.


## Branching

`git branch <new_branch_name>`

Creates a new "timeline" onto which you can add your work without interrupting or changing other "timeline."

`git checkout <target_branch>`

Allows you to move to another branch. Can use `git checkout <commit hash>` to move back to a previous commit, BUT you will be in a "detached head" state. If you want to branch from a previous version of your project, you can `git checkout -b <new_branch>` while you are in the "detached head" state to create a branch from that commit.

## Updating

`git merge <target_branch>`

Merges a target branch into current branch. Changes made on the same lines of code in both branches will cause conflicts which must be resolved and then committed. The merge commit will have 2 pointers pointing to the last commit of each branch since both are the parents of the merge.

`git rebase <target_branch>`

Takes entire current branch and moves the pointer for its base commit to the HEAD of the target branch. Creates a cleaner commit history, but is dangerous because the rebased commits will be a permanent part of the commit history of the target branch. 

## Deleting

`git stash`

	Temporarily stashes any changes since previous commit and saves it to the stash list. Use `git stash list` to see list of all stashes (stored in reverse order, i.e. 0 is the latest stash). `git stash apply` to apply all stashed changes to code, `git stash apply <stash identifier>` to apply a specific stash.

`git reset --hard <COMMIT HASH>`
	 
	WARNING: This is dangerous! This allows you to move to a previous commit and discard all commits made afterwards. This should only be done in extreme cases, such as when an API key or other important secret information gets accidentally pushed up and is a permanent part of the commit history. This will only affect your local repo; to get the reset repo to overwrite the repo on your remote, you must use `git push -f <remote> <branch>` to force your local repo's commit history onto the remote.