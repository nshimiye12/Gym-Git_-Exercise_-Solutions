# exercise 1 Bundle 1
``` PS C:\Users\Hp\Desktop\Exercise> git init
Initialized empty Git repository in C:/Users/Hp/Desktop/Exercise/.git/
PS C:\Users\Hp\Desktop\Exercise> git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\Hp\Desktop\Exercise> git branch -M main
PS C:\Users\Hp\Desktop\Exercise> git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\Hp\Desktop\Exercise> git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Hp\Desktop\Exercise> git add .\README.md
PS C:\Users\Hp\Desktop\Exercise> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md

PS C:\Users\Hp\Desktop\Exercise> git commit " init project"
error: pathspec ' init project' did not match any file(s) known to git
PS C:\Users\Hp\Desktop\Exercise> git commit -m " init project"
[main (root-commit) 4aebf05]  init project
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
PS C:\Users\Hp\Desktop\Exercise> git status
On branch main
nothing to commit, working tree clean
PS C:\Users\Hp\Desktop\Exercise> git remote add origin https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git
PS C:\Users\Hp\Desktop\Exercise> git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use        

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking     
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Hp\Desktop\Exercise>  git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 214 bytes | 107.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\Hp\Desktop\Exercise> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\Hp\Desktop\Exercise> git push origin dev 
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:        
remote:      https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions/pull/new/dev
remote:
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git     
 * [new branch]      dev -> dev
PS C:\Users\Hp\Desktop\Exercise> git checkout -b test 
Switched to a new branch 'test'
PS C:\Users\Hp\Desktop\Exercise> git push origin test 
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:       
remote:      https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions/pull/new/test
remote:
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git     
 * [new branch]      test -> test
PS C:\Users\Hp\Desktop\Exercise> git checkout dev
Switched to branch 'dev'
PS C:\Users\Hp\Desktop\Exercise> git branch -D test
Deleted branch test (was 4aebf05).
PS C:\Users\Hp\Desktop\Exercise> git push origin --delete test
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git
 - [deleted]         test
PS C:\Users\Hp\Desktop\Exercise> 

```
```
# exercise 2 Bundle1 
PS C:\Users\Hp\Desktop\Exercise> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Home.html

PS C:\Users\Hp\Desktop\Exercise> git checkout dev
Switched to branch 'dev'
A       Home.html
PS C:\Users\Hp\Desktop\Exercise> git reset
PS C:\Users\Hp\Desktop\Exercise> git status 
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)      
        Home.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Hp\Desktop\Exercise> git addd .\Home.html
git: 'addd' is not a git command. See 'git --help'.

The most similar command is
        add
PS C:\Users\Hp\Desktop\Exercise> git add .\Home.html 
PS C:\Users\Hp\Desktop\Exercise> git status 
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Home.html

PS C:\Users\Hp\Desktop\Exercise> git stash 
Saved working directory and index state WIP on dev: 4aebf05  init project
PS C:\Users\Hp\Desktop\Exercise> git stash list
stash@{0}: WIP on dev: 4aebf05 init project
PS C:\Users\Hp\Desktop\Exercise> git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)      
        about.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Hp\Desktop\Exercise> git add .\about.html
PS C:\Users\Hp\Desktop\Exercise> git stash
Saved working directory and index state WIP on dev: 4aebf05  init project
PS C:\Users\Hp\Desktop\Exercise> git stash list 
stash@{0}: WIP on dev: 4aebf05 init project
stash@{1}: WIP on dev: 4aebf05 init project
PS C:\Users\Hp\Desktop\Exercise> git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)      
        team.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Hp\Desktop\Exercise> git add .\team.html
PS C:\Users\Hp\Desktop\Exercise> git stash
Saved working directory and index state WIP on dev: 4aebf05  init project
PS C:\Users\Hp\Desktop\Exercise> git stash list
stash@{0}: WIP on dev: 4aebf05 init project
stash@{1}: WIP on dev: 4aebf05 init project
stash@{2}: WIP on dev: 4aebf05 init project

PS C:\Users\Hp\Desktop\Exercise> git stash pop
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (667475199e0361e4e8777d67c0a18c7abdfc9355)     
PS C:\Users\Hp\Desktop\Exercise> git add .\team.html
PS C:\Users\Hp\Desktop\Exercise> git stash 
PS C:\Users\Hp\Desktop\Exercise> git stash list  
stash@{0}: WIP on dev: 4aebf05 init project
stash@{1}: WIP on dev: 4aebf05 init project
stash@{2}: WIP on dev: 4aebf05 init project
PS C:\Users\Hp\Desktop\Exercise> git stash pop 'stash@{1}'
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (71ca75320eae8111d360649c7ab6767656edcfe7)
PS C:\Users\Hp\Desktop\Exercise> git stash list
stash@{0}: WIP on dev: 4aebf05 init project
stash@{1}: WIP on dev: 4aebf05 init project
PS C:\Users\Hp\Desktop\Exercise> git stash pop 'stash@{1}'
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Home.html
        new file:   about.html

Dropped stash@{1} (e038e8cc5a27db6c90c7479ccae6da149f839226)
PS C:\Users\Hp\Desktop\Exercise> git add --all
PS C:\Users\Hp\Desktop\Exercise> git status 
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Home.html
        new file:   about.html

PS C:\Users\Hp\Desktop\Exercise> git commit -m "setup the home and about page"
[dev 1c675c3] setup the home and about page
 2 files changed, 17 insertions(+)
 create mode 100644 Home.html
 create mode 100644 about.html
PS C:\Users\Hp\Desktop\Exercise> 
PS C:\Users\Hp\Desktop\Exercise> git stash list
stash@{0}: WIP on dev: 4aebf05 init project
PS C:\Users\Hp\Desktop\Exercise> git stash pop
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (a85d59913470d14fe1658ebd918bc519218416a0)
PS C:\Users\Hp\Desktop\Exercise> git reset --hard
HEAD is now at 1c675c3 setup the home and about page
PS C:\Users\Hp\Desktop\Exercise>
```
# bundle 2 Exercise 1
``` PS C:\Users\Hp\Desktop\Exercise> git checkout ft/bundle-2
error: pathspec 'ft/bundle-2' did not match any file(s) known to git
PS C:\Users\Hp\Desktop\Exercise> git checkout -b  ft/bundle-2
Switched to a new branch 'ft/bundle-2'
PS C:\Users\Hp\Desktop\Exercise> git status
On branch ft/bundle-2
nothing to commit, working tree clean
PS C:\Users\Hp\Desktop\Exercise> git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)      
        service.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Hp\Desktop\Exercise> git add .\service.html
PS C:\Users\Hp\Desktop\Exercise> git commit -m " create the service page"
[ft/bundle-2 c42ce1c]  create the service page
 1 file changed, 9 insertions(+)
 create mode 100644 service.html
PS C:\Users\Hp\Desktop\Exercise> git push 
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use        

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking     
upstream, see 'push.autoSetupRemote' in 'git help config'.git

PS C:\Users\Hp\Desktop\Exercise> git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 369 bytes | 369.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting 
remote:      https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git     
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
```
#  Bundle 2 Exercise 2
```
PS C:\Users\Hp\Desktop\Exercise> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\Hp\Desktop\Exercise> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Hp\Desktop\Exercise> git add .\README.md
PS C:\Users\Hp\Desktop\Exercise> git commit -m " new code added for Exercise 1 bundle 2"
[main 9b283e9]  new code added for Exercise 1 bundle 2
 1 file changed, 44 insertions(+)
PS C:\Users\Hp\Desktop\Exercise> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 698 bytes | 698.00 KiB/s, done.    
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git
   8ac255e..9b283e9  main -> main
PS C:\Users\Hp\Desktop\Exercise> git checkout ft/
error: pathspec 'ft/' did not match any file(s) known to git
PS C:\Users\Hp\Desktop\Exercise> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
PS C:\Users\Hp\Desktop\Exercise> git status
On branch ft/service-redesign
nothing to commit, working tree clean
PS C:\Users\Hp\Desktop\Exercise> git add --all
PS C:\Users\Hp\Desktop\Exercise> git status
On branch ft/service-redesign
Changes to be committed:
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use  

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.      

PS C:\Users\Hp\Desktop\Exercise> git push --set-upstream origin ft/service-redesign
fatal: unable to access 'https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git/': Could not resolve host: github.com   
PS C:\Users\Hp\Desktop\Exercise> git status
On branch ft/service-redesign
nothing to commit, working tree clean
PS C:\Users\Hp\Desktop\Exercise> git checkout -b ft/service-redesign
fatal: a branch named 'ft/service-redesign' already exists
PS C:\Users\Hp\Desktop\Exercise> git checkout ft/service-redesign
Already on 'ft/service-redesign'
PS C:\Users\Hp\Desktop\Exercise> git status 
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)    
  (use "git restore <file>..." to discard changes in working directory)
        modified:   service.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Hp\Desktop\Exercise> git add --all
PS C:\Users\Hp\Desktop\Exercise> git commit -m " some other feature added on service list "
[ft/service-redesign e0d3023]  some other feature added on service list
 1 file changed, 1 insertion(+)
PS C:\Users\Hp\Desktop\Exercise> git push 
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use  

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.      

PS C:\Users\Hp\Desktop\Exercise>  git push --set-upstream origin ft/service-redesign
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 691 bytes | 230.00 KiB/s, done.    
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign 
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
PS C:\Users\Hp\Desktop\Exercise> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Hp\Desktop\Exercise> git commit -m "add old services"
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)    
  (use "git restore <file>..." to discard changes in working directory)
        modified:   service.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Hp\Desktop\Exercise> git add .\service.html
PS C:\Users\Hp\Desktop\Exercise> git git push 
git: 'git' is not a git command. See 'git --help'.

The most similar command is
        init
PS C:\Users\Hp\Desktop\Exercise> git  push    
Everything up-to-date
PS C:\Users\Hp\Desktop\Exercise> git checkout ft/service-redesign
error: Your local changes to the following files would be overwritten by checkout:
        service.html
Please commit your changes or stash them before you switch branches.
Aborting
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
Merge branch 'main' into ft/service-redesign
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git
   9b283e9..5403b8c  main -> main
PS C:\Users\Hp\Desktop\Exercise> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.    
PS C:\Users\Hp\Desktop\Exercise> git merge main
Auto-merging service.html
CONFLICT (add/add): Merge conflict in service.html
[ft/service-redesign 5830015] Merge branch 'main' into ft/service-redesign
PS C:\Users\Hp\Desktop\Exercise> git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 431 bytes | 215.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git
   e0d3023..5830015  ft/service-redesign -> ft/service-redesign
PS C:\Users\Hp\Desktop\Exercise>
```