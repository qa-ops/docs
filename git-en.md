# GIT CLI

## Videos

All comands were explained, in a hands on approach, in my channel QaOps(http://videos.qa-ops.com/youtube
). 

* Playlist de UNIX(https://www.youtube.com/playlist?list=PLhJTa4U57yUsKBcqWbGaAQ7QpcgzKakVe)

## References

* https://git-scm.com/docs

## Commands

* `git clone <repo_url>` - clones a repository.    
* `git add <file>` - adds a file to the index(staging) for the next commit. 
* `git add -all` - adds all files in the working tree to the index(staging).
* `git add -p` - interactively adds peaces of changes to the index(staging).    
* `git commit` -  adds a new commit with the current content of the index(staging) and gives it a description message.
* `git commit -m 'commit message'` - creates the commit with the message in a single line.
* `git status` - shows the working tree status.     
* `git push` - updates remote repo with all local commits 
* `git pull` - gets all changes from remote repo. 
* `git branch` - lists all local branches.
* `git branch <nome>` - creates a new branch.
* `git checkout` - switches between branches or restores files from the working tree.
* `git checkout -b {branch}` - creates a new branch and switches to it.
* `git diff` - shows the differences between commits, working trees and etc.. 
* `git revert` - reverts a commit. 
* `git log` - show commit logs.
* `git log --grep='<descrição>'` - search commit by description
* `git merge <branch>` - do the merge of the current branch with the branch passed as parameter
