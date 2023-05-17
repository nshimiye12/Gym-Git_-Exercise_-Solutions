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
upstream, see 'push.autoSetupRemote' in 'git help config'.

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

# Bundle 3 Exercise 1 
PS C:\Users\Hp\Desktop\Exercise> git checkout ft/team-page
Switched to branch 'ft/team-page'
PS C:\Users\Hp\Desktop\Exercise> git add '.\team .html'
PS C:\Users\Hp\Desktop\Exercise> git status 
On branch ft/team-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team .html

PS C:\Users\Hp\Desktop\Exercise> git commit -m " feature add team page "
[ft/team-page aa751fa]  feature add team page
 1 file changed, 8 insertions(+)
 create mode 100644 team .html
PS C:\Users\Hp\Desktop\Exercise> git push 
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Hp\Desktop\Exercise> git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 351 bytes | 351.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.  
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions/pull/new/ft/team-page
remote:
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git     
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
PS C:\Users\Hp\Desktop\Exercise> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Hp\Desktop\Exercise> git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
PS C:\Users\Hp\Desktop\Exercise> git checkout ft/teampage
error: pathspec 'ft/teampage' did not match any file(s) known to git
PS C:\Users\Hp\Desktop\Exercise> git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
PS C:\Users\Hp\Desktop\Exercise> git log
commit aa751fa10707c3b9cf957a0876c8d36b19e3bdaa (HEAD -> ft/team-page,
 origin/ft/team-page)
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 10:30:25 2023 +0200

     feature add team page

commit 24f2328cc0c81936cfc3ffa743436cc974553333 (origin/main, main, ft/contact-page)
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 01:53:13 2023 +0200

    exercise2 bundle 2

commit 5403b8c03933947cecf5a4bba2cc6b61b5565798
Author: emery v <valery.emery02@gmail.com>
commit aa751fa10707c3b9cf957a0876c8d36b19e3bdaa (HEAD -> ft/team-page, origin/ft/team-page)
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 10:30:25 2023 +0200

     feature add team page

commit 24f2328cc0c81936cfc3ffa743436cc974553333 (origin/main, main, ft/contact-page)
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 01:53:13 2023 +0200

    exercise2 bundle 2

commit 5403b8c03933947cecf5a4bba2cc6b61b5565798
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 01:23:57 2023 +0200

     old features

commit 9b283e90c42182c21d09a159260f387b9c0a11c9
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 00:53:43 2023 +0200

     new code added for Exercise 1 bundle 2

commit 8ac255e5fd32b27abbba66096770bd568f0b980a
Author: emery v <valery.emery02@gmail.com>
PS C:\Users\Hp\Desktop\Exercise> git checkout ft/contact-page
Switched to branch 'ft/contact-page'
PS C:\Users\Hp\Desktop\Exercise> git cherry-pick
usage: git cherry-pick [--edit] [-n] [-m <parent-number>] [-s] [-x] [--ff]
                       [-S[<keyid>]] <commit>...
   or: git cherry-pick (--continue | --skip | --abort | --quit)       

    --quit                end revert or cherry-pick sequence
    --continue            resume revert or cherry-pick sequence       
    --abort               cancel revert or cherry-pick sequence       
    --skip                skip current commit and continue
    --cleanup <mode>      how to strip spaces and #comments from message
    -n, --no-commit       don't automatically commit
    -e, --edit            edit the commit message
    -s, --signoff         add a Signed-off-by trailer
    -m, --mainline <parent-number>
                          select mainline parent
    --rerere-autoupdate   update the index with reused conflict resolution if possible
    --strategy <strategy>
                          merge strategy
    -X, --strategy-option <option>
                          option for merge strategy
    -S, --gpg-sign[=<key-id>]
                          GPG sign commit
    -x                    append commit name
    --ff                  allow fast-forward
    --allow-empty         preserve initially empty commits
    --allow-empty-message
                          allow commits with empty messages
    --keep-redundant-commits
                          keep redundant, empty commits

PS C:\Users\Hp\Desktop\Exercise> git cherry-pick aa751fa10707c3b9cf957a0876c8d36b19e3bdaa
[ft/contact-page da88895]  feature add team page
 Date: Wed May 17 10:30:25 2023 +0200
 1 file changed, 8 insertions(+)
 create mode 100644 team .html
PS C:\Users\Hp\Desktop\Exercise> git log
commit da888951574177df87ffc0c33af26dfde5b0780e (HEAD -> ft/contact-page)
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 10:30:25 2023 +0200

     feature add team page

commit 24f2328cc0c81936cfc3ffa743436cc974553333 (origin/main, main)   
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 01:53:13 2023 +0200

    exercise2 bundle 2

commit 5403b8c03933947cecf5a4bba2cc6b61b5565798
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 01:23:57 2023 +0200

     old features

commit 9b283e90c42182c21d09a159260f387b9c0a11c9
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 00:53:43 2023 +0200

     new code added for Exercise 1 bundle 2

commit 8ac255e5fd32b27abbba66096770bd568f0b980a
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 00:47:00 2023 +0200
PS C:\Users\Hp\Desktop\Exercise> git status
On branch ft/contact-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)      
        contact.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Hp\Desktop\Exercise> git add .\contact.html
PS C:\Users\Hp\Desktop\Exercise> git commit -m " feature: add contact page"
[ft/contact-page dc0c08d]  feature: add contact page
 1 file changed, 8 insertions(+)
 create mode 100644 contact.html
PS C:\Users\Hp\Desktop\Exercise> git push 
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use        

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking     
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Hp\Desktop\Exercise> git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 665 bytes | 166.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.  
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git     
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
PS C:\Users\Hp\Desktop\Exercise> git status   
On branch ft/contact-page
Your branch is up to date with 'origin/ft/contact-page'.

nothing to commit, working tree clean
PS C:\Users\Hp\Desktop\Exercise> git checkout ft/faq-page
error: pathspec 'ft/faq-page' did not match any file(s) known to git
PS C:\Users\Hp\Desktop\Exercise> git checkout -b  ft/faq-page
Switched to a new branch 'ft/faq-page'
PS C:\Users\Hp\Desktop\Exercise> git add -all
error: did you mean `--all` (with two dashes)?
PS C:\Users\Hp\Desktop\Exercise> git add --all
PS C:\Users\Hp\Desktop\Exercise> git commit -m "feature :add FAQ-page"

[ft/faq-page 36c7ef1] feature :add FAQ-page
 1 file changed, 8 insertions(+)
 create mode 100644 faq.html
PS C:\Users\Hp\Desktop\Exercise> git push 
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use        

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking     
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Hp\Desktop\Exercise> git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 358 bytes | 179.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.  
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting 
remote:      https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git     
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
PS C:\Users\Hp\Desktop\Exercise> git log
commit 36c7ef15eabf42493939e6020555449de582f081 (HEAD -> ft/faq-page, origin/ft/faq-page)
Revert " feature add team page"
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 10:50:50 2023 +0200

    feature :add FAQ-page

commit dc0c08d0e4850b18239b96def8de8ea0edc0c1e9 (origin/ft/contact-page, ft/contact-page)
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 10:45:10 2023 +0200

     feature: add contact page

commit da888951574177df87ffc0c33af26dfde5b0780e
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 10:30:25 2023 +0200

     feature add team page

commit 24f2328cc0c81936cfc3ffa743436cc974553333 (origin/main, main)   
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 01:53:13 2023 +0200

 ```
    # exercise2 bundle 2

commit 5403b8c03933947cecf5a4bba2cc6b61b5565798
Author: emery v <valery.emery02@gmail.com>
PS C:\Users\Hp\Desktop\Exercise> git revert da888951574177df87ffc0c33af26dfde5b0780e
[ft/faq-page 460dce8] Revert " feature add team page"
 1 file changed, 8 deletions(-)
 delete mode 100644 team .html
PS C:\Users\Hp\Desktop\Exercise> git log
commit 460dce8d1ae5127eb60201e457631968787f2bd2 (HEAD -> ft/faq-page)
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 10:54:08 2023 +0200

    Revert " feature add team page"

    This reverts commit da888951574177df87ffc0c33af26dfde5b0780e.     

commit 36c7ef15eabf42493939e6020555449de582f081 (origin/ft/faq-page)
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 10:50:50 2023 +0200

    feature :add FAQ-page

commit dc0c08d0e4850b18239b96def8de8ea0edc0c1e9 (origin/ft/contact-page, ft/contact-page)
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 10:45:10 2023 +0200

     feature: add contact page

commit da888951574177df87ffc0c33af26dfde5b0780e
Author: emery v <valery.emery02@gmail.com>
Date:   Wed May 17 10:30:25 2023 +0200

     feature add team page

commit 24f2328cc0c81936cfc3ffa743436cc974553333 (origin/main, main)   
PS C:\Users\Hp\Desktop\Exercise> git push  
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 278 bytes | 278.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.  
To https://github.com/nshimiye12/Gym-Git_-Exercise_-Solutions.git
   36c7ef1..460dce8  ft/faq-page -> ft/faq-page
PS C:\Users\Hp\Desktop\Exercise> 

```