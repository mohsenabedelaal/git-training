# Git Training Notes 
##### Undo your uncommitted changes :
If you are working on your folder, and you have done some changes, and then you realized that these changes are causing bugs and you need to undo them all what you do using git :
1. You check the changes are tracked by git : `git status` 
2. Changes not staged for commit so in order to undo your changes : `git restore . ` or `git restore <file-name> `

##### Undo your committed changes :
If you are working on your folder , and you have committed some changes , and then you realized you don't need this commit you need to go to the previous commit without deleting this commit (go back in history to previous commit without deleting commits):

###### This if one commit 
1.  `git status` Check no changes
2. `git log` to take the commit hash that you want to revert from (copy commit hash)
3. `git revert <commit-hash>` 

###### This if more than one commit
1. `git log` to copy the commit hash of from where to where [first commit , where you need to revert to].
2. `git revert <first-commit>...<destination-commit>`

###### This if you want to revert to specific commit without commiting the revert
1. `git log` to copy the commit hash where you need to revert (go back in time with commit).
2. `git revert -n <destination-commit>`

##### Resetting changes :
If you want to go back in time to specific commit and you realized that after this commit all the changes are useless and you don't need them
