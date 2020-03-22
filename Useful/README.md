# Useful commands

## Pushing branches to remote repository
##### - git push origin < name of your branch >

## Pushing few times same commit
##### - git push origin < name of branch >
*^first time pushing a branch*
##### - git commit --amend
*Making some changes to the same commit which was already pushed, where --amend means commiting additional content to last commit.*
##### - git push origin < name of branch > -f 
*When you amend your last commit, you kinda bending your commit history. Therefore when you'll try to push it to remote repo, you'll be rejected. That's why you have to use "-f" --> force push. Use it carefully.*

## Branches handling

#### Listing your local branches
##### - git branch

#### Changing branch
##### - git checkout < name of branch >

#### Creating new branches
##### - git checkout -b < name_of_new_branch >

#### Deleting branches
##### - git checkout -d < name_of_branch_to_delete >    (safe)
##### - git checkout -D < name_of_branch_to_delete >    (not safe, but always works)
*Using "-D" is like force deleting branches. Using "-d" might cause git warnings, if you have some uncommited changes.*

#### Set upstream branch
##### - git branch --set-upstream-to=origin/< name_of_remote_branch >
*When you'll check status of your branch, you'll se how the local and remote branches have diverged. (E.g. how many commits is you local branch ahead of remote branch)

## Status
##### - git status
*Showes which files were changed, which were added already to staging level, which are untracked."
##### - git log -n (where n is number of commits that you'd like to see)
*Lists 'n' latest commits*
##### - git diff
*There are many options for using git diff. E.g. You can diff two commits by "git diff < commit A hash > < commit B hash >" or two files by "git diff

## Reseting
Deleting latest commits on a branch:
##### - git reset --hard HEAD~n (where n is number of commits that you'd like to delete)
##### - git reset --hard origin/master
*When you want to clear unstaged files. Clears all untracked directories (-d) with force (-f). Usefull to delete all build products.*
##### - git clean -df
*Remove untracked files from the working tree."

## Deleting files from git repo
##### - git rm <file_name>

## Cherry-picking
Takes commit from other branch to HEAD of current branch.
###### - git checkout < name_of_branch_where_you_want_to_add_commit >
###### - git cherry-pick < commit_sha_from_other_branch >

## Rebasing/merging
Rebase:
###### - git checkout < name_of_branch_that_you_want_to_rebase >
###### - git rebase master
*If you want to push to remote branch once again, you have to use force push.*
