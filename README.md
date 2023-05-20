ayyoo wassuppp

some git command that i don't frequently use besides `git add`, `git 
commit`, `git diff` etc.

- `git status`: show the status, if exists, or showing untracked files, 
changes to commited files, etc. changes on files that are put into 
`.gitignore` are not shown.

- `git log`: logs the commits. if none, shows `your current branch 'main' 
does not have any commits yet`. each commit has it's own hash, hence it 
helps to get back to previous commits.

- `HEAD`: it is a reference to the last commit in the currently 
checked-out branch. think of it like the 'current branch'. if you're 
coding on a different branch, say `fatma`, which is an 
experimental-branch, then the `HEAD` will point towards `fatma`.

- `git config --global core.editor "<choice_of_prefer>"` makes that if you 
try to commit without any message, it will appear the editor of 
`<choice_of_prefer>`.

- to create and switch automatically to newly created branch, enter `git 
checkout <newly_created_branch_name>, otherwise, enter `git switch <branch_name>`.
 
- to see the current `HEAD`, print `git branch`. after the creation of a
new branch. -> this article was copy-pasted from branch `fatma`. the changes 
made on another branch obviously doesn't change the others.

<<<<<<< HEAD
- to remove a file from local repository (after committing) — but not 
deleting from the **filesystem**, enter `git rm --cached <filename>`. if you 
want to delete from both local repository and filesystem, enter `git rm 
<filename>`.

- in order to remove a file from staging area; enter `git restore --staged 
<individual_file`.

- make sure the `HEAD` must be the merge-receiving branch. and then enter 
`git merge <branch_merged>` to merge two branches together.
=======
- THIS ARTICLE IS WRITTEN IN branch `to_be_merged` and will be merged to 
`main`.
>>>>>>> to_be_merged

- The `git stash` command takes your uncommitted changes (both staged and 
unstaged), faces them away for later use, and then reverts them from your 
working copy. Hence, you can work on other branches, perform any other Git 
operations. After, you can come back and re-apply your stash when you're 
ready. To re-apply stashed changes, just enter `git stash pop`. **NOTE:** 
in order to stash not just tracked files but also working directory, enter 
`git stash --include-untracked` or `git stash -u`. you can get info about 
stashes by using `git stash list`.

- to clear a stash, enter `git stash clear`.

- if you want to turn back to previous commits, then `git reset --hard 
<commit_hash>`. if `--hard` isn't used, then the commits are deleted by 
changes to files are remained.

- `git revert` simply used for undoing changes, without deleting the 
commits. thus all the commits will be saved in the `git log`.

- `git rebase` — or rebasing is the process of moving or combining a 
sequence of commits to a new base commit. the primary reason for rebasing 
is to maintain a linear project history.
