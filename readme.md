# Git Exercise

## Bundle 1

### Exercise 1

```bash
DavidEbun@davids-mbp ~ % cd desktop
DavidEbun@davids-mbp desktop % mkdir git-exercise
DavidEbun@davids-mbp desktop % cd git-exercise
DavidEbun@davids-mbp git-exercise % git init
DavidEbun@davids-mbp git-exercise % git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
DavidEbun@davids-mbp git-exercise % git branch -m main
DavidEbun@davids-mbp git-exercise % git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
DavidEbun@davids-mbp git-exercise % git add readme.md
DavidEbun@davids-mbp git-exercise % git commit -m "Git Exercise"
[main (root-commit) 10b6521] Git Exercise
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 readme.md
DavidEbun@davids-mbp git-exercise % git remote add origin https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
DavidEbun@davids-mbp git-exercise % git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 223 bytes | 223.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
DavidEbun@davids-mbp git-exercise % git branch dev
DavidEbun@davids-mbp git-exercise % git branch
  dev
* main
DavidEbun@davids-mbp git-exercise % git checkout dev
M       readme.md
Switched to branch 'dev'
DavidEbun@davids-mbp git-exercise % git checkout -b test
Switched to a new branch 'test'
DavidEbun@davids-mbp git-exercise % git checkout dev
M       readme.md
Switched to branch 'dev'
DavidEbun@davids-mbp git-exercise % git branch -d test
Deleted branch test (was 10b6521).
DavidEbun@davids-mbp git-exercise % git branch
* dev
  main
```

### Exercise 2

```bash

DavidEbun@davids-mbp git-exercise % git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

no changes added to commit (use "git add" and/or "git commit -a")
DavidEbun@davids-mbp git-exercise % git stash list
DavidEbun@davids-mbp git-exercise % git add home.html
DavidEbun@davids-mbp git-exercise % git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

DavidEbun@davids-mbp git-exercise % git stash
Saved working directory and index state WIP on dev: 10b6521 Git Exercise
DavidEbun@davids-mbp git-exercise % git stash list
stash@{0}: WIP on dev: 10b6521 Git Exercise
DavidEbun@davids-mbp git-exercise % git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)
DavidEbun@davids-mbp git-exercise % git add about.html
DavidEbun@davids-mbp git-exercise % git stash
Saved working directory and index state WIP on dev: 10b6521 Git Exercise
DavidEbun@davids-mbp git-exercise % git stash list
stash@{0}: WIP on dev: 10b6521 Git Exercise
stash@{1}: WIP on dev: 10b6521 Git Exercise
DavidEbun@davids-mbp git-exercise % git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
DavidEbun@davids-mbp git-exercise % git add team.html
DavidEbun@davids-mbp git-exercise % git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

DavidEbun@davids-mbp git-exercise % git stash
Saved working directory and index state WIP on dev: 10b6521 Git Exercise
DavidEbun@davids-mbp git-exercise % git stash list
stash@{0}: WIP on dev: 10b6521 Git Exercise
stash@{1}: WIP on dev: 10b6521 Git Exercise
stash@{2}: WIP on dev: 10b6521 Git Exercise
DavidEbun@davids-mbp git-exercise %

DavidEbun@davids-mbp git-exercise % git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (384524e59411a7552954ae754f095752cd758b5d)
DavidEbun@davids-mbp git-exercise % git stash list
stash@{0}: WIP on dev: 10b6521 Git Exercise
stash@{1}: WIP on dev: 10b6521 Git Exercise
DavidEbun@davids-mbp git-exercise % git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (c0806839eca5f96a185d70056750b2b118885c78)
DavidEbun@davids-mbp git-exercise % git commit -m "setting up the home and about pages"
[dev 9002313] setting up the home and about pages
 2 files changed, 71 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
DavidEbun@davids-mbp git-exercise % git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

DavidEbun@davids-mbp git-exercise % git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 2.42 KiB | 1.21 MiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
 * [new branch]      dev -> dev
DavidEbun@davids-mbp git-exercise % git push --set-upstream origin dev
branch 'dev' set up to track 'origin/dev'.
Everything up-to-date
DavidEbun@davids-mbp git-exercise % git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean
DavidEbun@davids-mbp git-exercise % git stash list
stash@{0}: WIP on dev: 10b6521 Git Exercise
DavidEbun@davids-mbp git-exercise % git stash pop
On branch dev
Your branch is behind 'origin/dev' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (06c7380989a17746f50059f9b332c9a70e5f0904)
DavidEbun@davids-mbp git-exercise % git reset --hard
HEAD is now at 9002313 setting up the home and about pages
DavidEbun@davids-mbp git-exercise % git status
On branch dev
Your branch is behind 'origin/dev' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

nothing to commit, working tree clean

```

## Bundle 2

### Exercise 1

```bash
DavidEbun@davids-mbp git-exercise % git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
DavidEbun@davids-mbp git-exercise % git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        service.html

nothing added to commit but untracked files present (use "git add" to track)
DavidEbun@davids-mbp git-exercise % git add service.html
DavidEbun@davids-mbp git-exercise % git status
On branch ft/bundle-2
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   service.html

DavidEbun@davids-mbp git-exercise % git commit -m "created a service page"
[ft/bundle-2 f8f28d9] created a service page
 1 file changed, 18 insertions(+)
 create mode 100644 service.html
DavidEbun@davids-mbp git-exercise % git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

DavidEbun@davids-mbp git-exercise %  git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 688 bytes | 688.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

```

### Exercise 2

```bash
DavidEbun@davids-mbp git-exercise % git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 4 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
DavidEbun@davids-mbp git-exercise % git pull
Updating 10b6521..234c19b
Fast-forward
 about.html   | 31 +++++++++++++++++++++++++++++++
 home.html    | 40 ++++++++++++++++++++++++++++++++++++++++
 service.html | 18 ++++++++++++++++++
 3 files changed, 89 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 service.html
DavidEbun@davids-mbp git-exercise % git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
DavidEbun@davids-mbp git-exercise % git branch
  dev
  ft/bundle-2
* ft/service-redesign
  main
DavidEbun@davids-mbp git-exercise % git add --a
DavidEbun@davids-mbp git-exercise % git status
On branch ft/service-redesign
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   service.html

DavidEbun@davids-mbp git-exercise % git commit -m "Service Page Modified"
[ft/service-redesign c3f6c98] Service Page Modified
 1 file changed, 10 insertions(+), 5 deletions(-)
DavidEbun@davids-mbp git-exercise % git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

DavidEbun@davids-mbp git-exercise % git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 473 bytes | 473.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
DavidEbun@davids-mbp git-exercise % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
DavidEbun@davids-mbp git-exercise % git add --a
DavidEbun@davids-mbp git-exercise % git commit -m "made changes on the main branch to the Service page"
[main 217c6b2] made changes on the main branch to the Service page
 1 file changed, 7 insertions(+), 5 deletions(-)
DavidEbun@davids-mbp git-exercise % git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 453 bytes | 453.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
   234c19b..217c6b2  main -> main
DavidEbun@davids-mbp git-exercise % git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
DavidEbun@davids-mbp git-exercise % git merge main
Auto-merging service.html
CONFLICT (content): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.
DavidEbun@davids-mbp git-exercise % git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   service.html

DavidEbun@davids-mbp git-exercise % git commit
[ft/service-redesign 51f75c5] Merge branch 'main' into ft/service-redesign
DavidEbun@davids-mbp git-exercise % git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 509 bytes | 509.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
   c3f6c98..51f75c5  ft/service-redesign -> ft/service-redesign
DavidEbun@davids-mbp git-exercise % git branch
  dev
  ft/bundle-2
* ft/service-redesign
  main
DavidEbun@davids-mbp git-exercise % git diff main
diff --git a/service.html b/service.html
index 453a325..b6ea25c 100644
--- a/service.html
+++ b/service.html
@@ -8,10 +8,17 @@
   <body>
     <h1>Service Offered</h1>
     <p>
-      We are dedicated to providing our clients with a wide array of top-notch services
-      that cater to their unique needs and aspirations.
+      At [Company Name], we are dedicated to providing our clients with a wide array of
+      top-notch services that cater to their unique needs and aspirations. With our
+      expertise, innovation, and unwavering commitment to excellence, we offer a diverse
+      range of services designed to surpass expectations and drive exceptional results.
+      Explore our comprehensive service offerings:
     </p>
-    <h2>Services</h2>
+
+    <p>
+      We offer a diverse range of services designed to surpass expectations and drive
+      exceptional results. Explore our comprehensive service offerings:
+    </p
     <ul>
       <li>Customized Solutions</li>
       <li>Innovative Product Development</li>
DavidEbun@davids-mbp git-exercise % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
DavidEbun@davids-mbp git-exercise % git merge ft/service-redesign
Updating 217c6b2..51f75c5
Fast-forward
 service.html | 13 ++++++++++---
 1 file changed, 10 insertions(+), 3 deletions(-)
DavidEbun@davids-mbp git-exercise % git commit -m "merged main with the service-redesign branch"
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
DavidEbun@davids-mbp git-exercise % git push
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
   217c6b2..51f75c5  main -> main
```

## Bundle 3

### Exercise 1

```bash
DavidEbun@davids-mbp git-exercise % git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
DavidEbun@davids-mbp git-exercise % git add team.html
DavidEbun@davids-mbp git-exercise % git status
On branch ft/team-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

DavidEbun@davids-mbp git-exercise % git commit -m "added team page"
[ft/team-page d2718d2] added team page
 1 file changed, 19 insertions(+)
 create mode 100644 team.html
DavidEbun@davids-mbp git-exercise % git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

DavidEbun@davids-mbp git-exercise %  git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 556 bytes | 278.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
DavidEbun@davids-mbp git-exercise % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
DavidEbun@davids-mbp git-exercise % git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
DavidEbun@davids-mbp git-exercise % git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
DavidEbun@davids-mbp git-exercise % git log
commit d2718d22bb6ceebca4baccd283b271d08dc4c46c (HEAD -> ft/team-page, origin/ft/team-page)
Author: DAVIDEbun <ebunoluwadamilare@gmail.com>
Date:   Tue Jun 27 12:19:16 2023 +0100

    added team page

commit 51f75c567ae13336d5900792568db0d486e292b7 (origin/main, origin/ft/service-redesign, main, ft/service-redesign, ft/contact-page)
Merge: c3f6c98 217c6b2
Author: DAVIDEbun <ebunoluwadamilare@gmail.com>
Date:   Tue Jun 27 11:43:57 2023 +0100

    Merge branch 'main' into ft/service-redesign

commit 217c6b217ada998bf196759a0d825352a83c2ca9
Author: DAVIDEbun <ebunoluwadamilare@gmail.com>
Date:   Tue Jun 27 11:18:16 2023 +0100

    made changes on the main branch to the Service page

commit c3f6c98ab5f9da271b92450fe394caea537354a5
Author: DAVIDEbun <ebunoluwadamilare@gmail.com>
Date:   Tue Jun 27 11:12:49 2023 +0100

    Service Page Modified

commit 234c19b03619f8daff415b0413cd35edf9184bb4
Merge: 27d0066 f8f28d9
Author: Ebunoluwa David <ebunoluwadamilare@gmail.com>
Date:   Tue Jun 27 11:02:39 2023 +0100

    Merge pull request #3 from DAVIDEbun/ft/bundle-2

DavidEbun@davids-mbp git-exercise % :bq
zsh: command not found: :bq
DavidEbun@davids-mbp git-exercise % git checkout ft/contact-page
Switched to branch 'ft/contact-page'
DavidEbun@davids-mbp git-exercise % git cherry-pick d2718d22bb6ceebca4baccd283b271d08dc4c46c
[ft/contact-page c5e8e62] added team page
 Date: Tue Jun 27 12:19:16 2023 +0100
 1 file changed, 19 insertions(+)
 create mode 100644 team.html
DavidEbun@davids-mbp git-exercise % git log
commit c5e8e62951a49a7383f89fc7e26499f313e26c1f (HEAD -> ft/contact-page)
Author: DAVIDEbun <ebunoluwadamilare@gmail.com>
Date:   Tue Jun 27 12:19:16 2023 +0100

    added team page

commit 51f75c567ae13336d5900792568db0d486e292b7 (origin/main, origin/ft/service-redesign, main, ft/service-redesign)
Merge: c3f6c98 217c6b2
Author: DAVIDEbun <ebunoluwadamilare@gmail.com>
Date:   Tue Jun 27 11:43:57 2023 +0100

    Merge branch 'main' into ft/service-redesign

commit 217c6b217ada998bf196759a0d825352a83c2ca9
Author: DAVIDEbun <ebunoluwadamilare@gmail.com>
Date:   Tue Jun 27 11:18:16 2023 +0100

    made changes on the main branch to the Service page

commit c3f6c98ab5f9da271b92450fe394caea537354a5
Author: DAVIDEbun <ebunoluwadamilare@gmail.com>
Date:   Tue Jun 27 11:12:49 2023 +0100

    Service Page Modified

commit 234c19b03619f8daff415b0413cd35edf9184bb4
Merge: 27d0066 f8f28d9
Author: Ebunoluwa David <ebunoluwadamilare@gmail.com>
Date:   Tue Jun 27 11:02:39 2023 +0100

    Merge pull request #3 from DAVIDEbun/ft/bundle-2

DavidEbun@davids-mbp git-exercise % git add --a
DavidEbun@davids-mbp git-exercise % git status
On branch ft/contact-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   contact.html

DavidEbun@davids-mbp git-exercise % git commit -m "added contact page"
[ft/contact-page 83fbcab] added contact page
 1 file changed, 16 insertions(+)
 create mode 100644 contact.html
DavidEbun@davids-mbp git-exercise % git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

DavidEbun@davids-mbp git-exercise %  git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 1.06 KiB | 1.06 MiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
DavidEbun@davids-mbp git-exercise % git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
DavidEbun@davids-mbp git-exercise % git add --a
DavidEbun@davids-mbp git-exercise % git commit -m "added the FAQ Page feature"
[ft/faq-page 8285b5a] added the FAQ Page feature
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html
DavidEbun@davids-mbp git-exercise % git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

DavidEbun@davids-mbp git-exercise % git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 453 bytes | 453.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
DavidEbun@davids-mbp git-exercise % git revert d2718d22bb6ceebca4baccd283b271d08dc4c46c
hint: Waiting for your editor to close the file... error: There was a problem with the editor 'vi'.
Please supply the message using either -m or -F option.
```

## Bundle 4

### Exercise 1

```bash
DavidEbun@davids-mbp git-exercise % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
DavidEbun@davids-mbp git-exercise %  git remote add git-copy https://github.com/DAVIDEbun/The-Gym-Exercise-Copy.git
DavidEbun@davids-mbp git-exercise % git add --a
DavidEbun@davids-mbp git-exercise % git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   home.html

DavidEbun@davids-mbp git-exercise % git commit -m "restructured paragraph"
[main 1bf1d96] restructured paragraph
 1 file changed, 10 insertions(+), 14 deletions(-)
DavidEbun@davids-mbp git-exercise % git push origin
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 429 bytes | 429.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
   e144a94..1bf1d96  main -> main
DavidEbun@davids-mbp git-exercise % git push git-copy
Enumerating objects: 27, done.
Counting objects: 100% (27/27), done.
Delta compression using up to 4 threads
Compressing objects: 100% (25/25), done.
Writing objects: 100% (27/27), 6.08 KiB | 1.01 MiB/s, done.
Total 27 (delta 13), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (13/13), done.
To https://github.com/DAVIDEbun/The-Gym-Exercise-Copy.git
 * [new branch]      main -> main
```

### Exercise 2

```bash
DavidEbun@davids-mbp git-exercise % git checkout -b ft/footer
Switched to a new branch 'ft/footer'
DavidEbun@davids-mbp git-exercise % git add footer.html
DavidEbun@davids-mbp git-exercise % git status
On branch ft/footer
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   footer.html

DavidEbun@davids-mbp git-exercise % git commit -m "added footer page"
[ft/footer 70ced65] added footer page
 1 file changed, 33 insertions(+)
 create mode 100644 footer.html
DavidEbun@davids-mbp git-exercise % git add footer.html
DavidEbun@davids-mbp git-exercise % git commit -m "modified the footer content"
[ft/footer ea34127] modified the footer content
 1 file changed, 2 insertions(+), 4 deletions(-)
DavidEbun@davids-mbp git-exercise % git push
fatal: The current branch ft/footer has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/footer

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

DavidEbun@davids-mbp git-exercise %  git push --set-upstream origin ft/footer
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 1.01 KiB | 1.01 MiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions/pull/new/ft/footer
remote:
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.
DavidEbun@davids-mbp git-exercise % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
DavidEbun@davids-mbp git-exercise % git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'
DavidEbun@davids-mbp git-exercise % git merge --squash ft/footer
Updating 1bf1d96..ea34127
Fast-forward
Squash commit -- not updating HEAD
 footer.html | 31 +++++++++++++++++++++++++++++++
 1 file changed, 31 insertions(+)
 create mode 100644 footer.html
DavidEbun@davids-mbp git-exercise % git add --a
DavidEbun@davids-mbp git-exercise % git status
On branch ft/squashing
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   footer.html

DavidEbun@davids-mbp git-exercise % git commit -m "footer changes squashing"
[ft/squashing ea02953] footer changes squashing
 1 file changed, 31 insertions(+)
 create mode 100644 footer.html
DavidEbun@davids-mbp git-exercise % git push
fatal: The current branch ft/squashing has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/squashing

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

DavidEbun@davids-mbp git-exercise % git push --set-upstream origin ft/squashing
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 724 bytes | 724.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions/pull/new/ft/squashing
remote:
To https://github.com/DAVIDEbun/The-Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.
```

## Bundle 5

### Exercise 2

```bash
DavidEbun@davids-mbp ~ % cd desktop
DavidEbun@davids-mbp desktop % git clone https://github.com/DAVIDEbun/git-cafe-exercise.git
Cloning into 'git-cafe-exercise'...
remote: Enumerating objects: 107, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 107 (delta 5), reused 4 (delta 4), pack-reused 95
Receiving objects: 100% (107/107), 1.95 MiB | 679.00 KiB/s, done.
Resolving deltas: 100% (5/5), done.
DavidEbun@davids-mbp desktop % cd git-cafe-exercise
DavidEbun@davids-mbp git-cafe-exercise % git add index.html
DavidEbun@davids-mbp git-cafe-exercise % git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index.html

DavidEbun@davids-mbp git-cafe-exercise % git commit -m "renamed the content title"
[main f624cc7] renamed the content title
 1 file changed, 379 insertions(+), 239 deletions(-)
DavidEbun@davids-mbp git-cafe-exercise % git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.50 KiB | 1.50 MiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/DAVIDEbun/git-cafe-exercise.git
   d1d3f9c..f624cc7  main -> main
```

## Bundle 6

### Exercise 1

```bash
DavidEbun@davids-mbp git-cafe-exercise % git checkout -b ft/menu
Switched to a new branch 'ft/menu'
DavidEbun@davids-mbp git-cafe-exercise % git add menu.html
DavidEbun@davids-mbp git-cafe-exercise % git status
On branch ft/menu
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   menu.html

DavidEbun@davids-mbp git-cafe-exercise % git commit -m "added a feature, menu page"
[ft/menu 0d21934] added a feature, menu page
 1 file changed, 11 insertions(+)
 create mode 100644 menu.html
DavidEbun@davids-mbp git-cafe-exercise % git push
fatal: The current branch ft/menu has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/menu

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

DavidEbun@davids-mbp git-cafe-exercise %  git push --set-upstream origin ft/menu
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 462 bytes | 462.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/menu' on GitHub by visiting:
remote:      https://github.com/DAVIDEbun/git-cafe-exercise/pull/new/ft/menu
remote:
To https://github.com/DAVIDEbun/git-cafe-exercise.git
 * [new branch]      ft/menu -> ft/menu
branch 'ft/menu' set up to track 'origin/ft/menu'.
```

### Exercise 2

```bash
DavidEbun@davids-mbp git-cafe-exercise % git checkout -b bug-fix
Switched to a new branch 'bug-fix'
DavidEbun@davids-mbp git-cafe-exercise % git add --a
DavidEbun@davids-mbp git-cafe-exercise % git status
On branch bug-fix
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index-4.html

DavidEbun@davids-mbp git-cafe-exercise % git commit -m "changed title to Contact"
[bug-fix 100b433] changed title to Contact
 1 file changed, 212 insertions(+), 164 deletions(-)
DavidEbun@davids-mbp git-cafe-exercise % git push
fatal: The current branch bug-fix has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin bug-fix

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

DavidEbun@davids-mbp git-cafe-exercise % git push --set-upstream origin bug-fix
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.37 KiB | 1.37 MiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'bug-fix' on GitHub by visiting:
remote:      https://github.com/DAVIDEbun/git-cafe-exercise/pull/new/bug-fix
remote:
To https://github.com/DAVIDEbun/git-cafe-exercise.git
 * [new branch]      bug-fix -> bug-fix
branch 'bug-fix' set up to track 'origin/bug-fix'.
```

### Exercise 3

```bash
DavidEbun@davids-mbp git-cafe-exercise % git checkout -b hotfix
Switched to a new branch 'hotfix'
DavidEbun@davids-mbp git-cafe-exercise % git add --a
DavidEbun@davids-mbp git-cafe-exercise % git status
On branch hotfix
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index-4.html

DavidEbun@davids-mbp git-cafe-exercise % git commit -m "changed telephone number"
[hotfix f165b99] changed telephone number
 1 file changed, 200 insertions(+), 124 deletions(-)
DavidEbun@davids-mbp git-cafe-exercise % git push
fatal: The current branch hotfix has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin hotfix

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

DavidEbun@davids-mbp git-cafe-exercise % git push --set-upstream origin hotfix
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.37 KiB | 1.37 MiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'hotfix' on GitHub by visiting:
remote:      https://github.com/DAVIDEbun/git-cafe-exercise/pull/new/hotfix
remote:
To https://github.com/DAVIDEbun/git-cafe-exercise.git
 * [new branch]      hotfix -> hotfix
branch 'hotfix' set up to track 'origin/hotfix'.
```
