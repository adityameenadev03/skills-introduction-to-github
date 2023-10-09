<!-- Merging in git -->

create seperate branch
commit changes in that branch
git checkout the branch with which you want to merge you code into
run git merge <branchName>
now resolve any merge conflict
run git commit

 <!--the merge commit may include the commit info like which branches you have merged   -->

 <!-- to undo git merge (when you have not commited the changes) -->

1. git reset ( but then you have to unstage the staged file )

<!-- to get merge commit hash u can use git reflog -->

git reflog

<!-- undo the git merge -->

2. git reset --hard <merge-commit-hash>

<!-- You can also use git revert -->
<!-- git revert. => if merge is pushed into github. This creates a new commit that undoes the changes introduced by the merge.
 -->
<!-- you will have to commit the changes to complete the revert -->

3. git revert -m <merge-commit-hash>

<!-- remove the file from staging area -->

<!-- Unstage a file (move changes from the staging area back to the working directory -->

git resotre --staged <fileName>

<!-- Remove a file from both the working directory and the repository, then stage the deletion: -->

git rm <fileName>

<!-- Unstage changes but keep them in the working directory: -->

git reset --mixed
