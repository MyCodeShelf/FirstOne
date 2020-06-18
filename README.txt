Fix done Finally

C:\Git\FirstOne>git branch -r

C:\Git\FirstOne>git branch

C:\Git\FirstOne>git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

C:\Git\FirstOne>echo "FirstOne">>README.md

C:\Git\FirstOne>git init
Reinitialized existing Git repository in C:/Git/FirstOne/.git/

C:\Git\FirstOne>git add
Nothing specified, nothing added.
Maybe you wanted to say 'git add .'?

C:\Git\FirstOne>git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

C:\Git\FirstOne>git add README.md

C:\Git\FirstOne> git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 233 bytes | 38.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/rajputszapp/FirstOne.git
 * [new branch]      master -> master

C:\Git\FirstOne>git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

C:\Git\FirstOne>git status
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

C:\Git\FirstOne>git add README.md

C:\Git\FirstOne>git commit
Aborting commit due to empty commit message.

C:\Git\FirstOne>
C:\Git\FirstOne>
C:\Git\FirstOne>git commit -m "Updated msg"
[master 1be2a79] Updated msg
 1 file changed, 1 insertion(+)

C:\Git\FirstOne>git diff

C:\Git\FirstOne>git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 280 bytes | 93.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/rajputszapp/FirstOne.git
   e82e8cf..1be2a79  master -> master

C:\Git\FirstOne>git branch -r
  origin/master

C:\Git\FirstOne>git log
commit 1be2a793800f8b29003a9e50748b21bf86e65bcf (HEAD -> master, origin/master)
Author: rajputszapp <vikaschauhanmail@gmail.com>
Date:   Mon Apr 27 02:18:06 2020 +0530

    Updated msg

commit e82e8cfae36113dc7ba0810140957272ade7d214
Author: rajputszapp <vikaschauhanmail@gmail.com>
Date:   Mon Apr 27 01:23:45 2020 +0530

    First Commit

C:\Git\FirstOne>git diff

C:\Git\FirstOne>git difftool HEAD

C:\Git\FirstOne>
C:\Git\FirstOne>git checkout -b experimentalBranch
Switched to a new branch 'experimentalBranch'

C:\Git\FirstOne>git branch
* experimentalBranch
  master

C:\Git\FirstOne>git status
On branch experimentalBranch
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

C:\Git\FirstOne>git add README.md

C:\Git\FirstOne>git commit -m "Commited by experimental Branch"
[experimentalBranch 5ab5282] Commited by experimental Branch
 1 file changed, 1 insertion(+)

C:\Git\FirstOne>git branch
* experimentalBranch
  master

C:\Git\FirstOne>git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

C:\Git\FirstOne>git merge
Already up to date.

C:\Git\FirstOne>git checkout experimentalBranch
Switched to branch 'experimentalBranch'

C:\Git\FirstOne>git merge
fatal: No remote for the current branch.

C:\Git\FirstOne>git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

C:\Git\FirstOne>git log
commit 1be2a793800f8b29003a9e50748b21bf86e65bcf (HEAD -> master, origin/master)
Author: rajputszapp <vikaschauhanmail@gmail.com>
Date:   Mon Apr 27 02:18:06 2020 +0530

    Updated msg

commit e82e8cfae36113dc7ba0810140957272ade7d214
Author: rajputszapp <vikaschauhanmail@gmail.com>
Date:   Mon Apr 27 01:23:45 2020 +0530

    First Commit

C:\Git\FirstOne>git checkout experimentalBranch
Switched to branch 'experimentalBranch'

C:\Git\FirstOne>git log
commit 5ab52828a8f6274f0f02bc1dd3447c4b39d7c2d2 (HEAD -> experimentalBranch)
Author: rajputszapp <vikaschauhanmail@gmail.com>
Date:   Mon Apr 27 02:58:07 2020 +0530

    Commited by experimental Branch

commit 1be2a793800f8b29003a9e50748b21bf86e65bcf (origin/master, master)
Author: rajputszapp <vikaschauhanmail@gmail.com>
Date:   Mon Apr 27 02:18:06 2020 +0530

    Updated msg

commit e82e8cfae36113dc7ba0810140957272ade7d214
Author: rajputszapp <vikaschauhanmail@gmail.com>
Date:   Mon Apr 27 01:23:45 2020 +0530

    First Commit

C:\Git\FirstOne>git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

C:\Git\FirstOne>git status
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

C:\Git\FirstOne>git add README.md

C:\Git\FirstOne>git commit -m "New changes in master"
[master ec8fcf0] New changes in master
 1 file changed, 1 insertion(+)

C:\Git\FirstOne>git checkout experimentalBranch
Switched to branch 'experimentalBranch'

C:\Git\FirstOne>git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

C:\Git\FirstOne>git merge experimentalBranch
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

C:\Git\FirstOne>git merge experimentalBranch
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

C:\Git\FirstOne>git merge experimentalBranch
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

C:\Git\FirstOne>git checkout master
error: you need to resolve your current index first
README.md: needs merge

C:\Git\FirstOne>git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 314 bytes | 314.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/rajputszapp/FirstOne.git
   1be2a79..ec8fcf0  master -> master

C:\Git\FirstOne>git merge experimentalBranch
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

C:\Git\FirstOne>git checkout experimentalBranch
error: you need to resolve your current index first
README.md: needs merge

C:\Git\FirstOne>git checkout experimentalBranch
error: you need to resolve your current index first
README.md: needs merge

C:\Git\FirstOne>git reset --merge

C:\Git\FirstOne>git checkout master
Already on 'master'
Your branch is up to date with 'origin/master'.

C:\Git\FirstOne>git checkout experimentalBranch
Switched to branch 'experimentalBranch'

C:\Git\FirstOne>git status
On branch experimentalBranch
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

C:\Git\FirstOne>git add README.md

C:\Git\FirstOne>git commit -m "Commited new content"
[experimentalBranch 81719d6] Commited new content
 1 file changed, 1 insertion(+)

C:\Git\FirstOne>git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

C:\Git\FirstOne>git merge experimentalBranch
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

C:\Git\FirstOne>git reset --merge

C:\Git\FirstOne>git checkout experimentalBranch
Switched to branch 'experimentalBranch'

C:\Git\FirstOne>git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

C:\Git\FirstOne>git merge experimentalBranch
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

C:\Git\FirstOne>git merge experimentalBranch -move/left
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

C:\Git\FirstOne>git reset --merge

C:\Git\FirstOne>git merge experimentalBranch -move/left
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

C:\Git\FirstOne>git merge experimentalBranch
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

C:\Git\FirstOne>git checkout experimentalBranch
Switched to branch 'experimentalBranch'

C:\Git\FirstOne>git push
fatal: The current branch experimentalBranch has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin experimentalBranch


C:\Git\FirstOne>git status
On branch experimentalBranch
nothing to commit, working tree clean

C:\Git\FirstOne> git push --set-upstream origin experimentalBranch
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 622 bytes | 155.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'experimentalBranch' on GitHub by visiting:
remote:      https://github.com/rajputszapp/FirstOne/pull/new/experimentalBranch
remote:
To https://github.com/rajputszapp/FirstOne.git
 * [new branch]      experimentalBranch -> experimentalBranch
Branch 'experimentalBranch' set up to track remote branch 'experimentalBranch' from 'origin'.

C:\Git\FirstOne>git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.