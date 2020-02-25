# Useful commands

## Pushing branches to remote repo
- git push origin <nam of branch>

## Pushing few times same commit
- git push origin <nam of branch>
- git commit --amend
- git push origin <nam of branch> -f 
##### where "-f" means force push (use very carefully)

## Handling of branches

#### Creating new branches
- git checkout -b <name_of_new_branch>

#### Deleting branches
- git checkout -d <name_of_branch_to_delete> (safe)
- git checkout -D <name_of_branch_to_delete> (not safe, but )

#### Set upstream branch
- git branch --set-upstream-to=origin/<name_of_remote_branch>


## Status
- git status
- git log -n (where n is number of commits that you'd like to see)
- git diff


## Reseting
- git reset --hard HEAD~n (where n is number of commits that you'd like to delete)
- git reset --hard origin/master
- git clean -df


## Cherry-picking
Takes commit from other branch to HEAD of current branch.
- git checkout <name_of_branch_where_you_want_to_add_commit>
- git cherry-pick <commit_sha_from_other_branch>


## Rebasing/merging
Rebase:
- git checkout <name_of_branch>
- git rebase master
If you want to push to remote branch once again, you have to use force push.

