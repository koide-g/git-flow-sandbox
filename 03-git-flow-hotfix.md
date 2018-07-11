## git flow release


```
[develop] % git flow hotfix start 0.1.1
Switched to a new branch 'hotfix/0.1.1'

Summary of actions:
- A new branch 'hotfix/0.1.1' was created, based on 'master'
- You are now on branch 'hotfix/0.1.1'

Follow-up actions:
- Start committing your hot fixes
- Bump the version number now!
- When done, run:

     git flow hotfix finish '0.1.1'

[0.1.1] % git commit -am 'remove version from readme'
[hotfix/0.1.1 0cf801b] remove version from readme
 1 file changed, 2 deletions(-)
[0.1.1] % git commit -am 'bump v0.1.1'
[hotfix/0.1.1 ebe6300] bump v0.1.1
 1 file changed, 1 insertion(+), 1 deletion(-)


[0.1.1] % git flow hotfix publish
Counting objects: 6, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 599 bytes | 599.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0)
To github.com:koide-g/git-flow-sandbox.git
 * [new branch]      hotfix/0.1.1 -> hotfix/0.1.1
Branch 'hotfix/0.1.1' set up to track remote branch 'hotfix/0.1.1' from 'origin'.
Already on 'hotfix/0.1.1'
Your branch is up to date with 'origin/hotfix/0.1.1'.

Summary of actions:
- The remote branch 'hotfix/0.1.1' was created or updated
- The local branch 'hotfix/0.1.1' was configured to track the remote branch
- You are now on branch 'hotfix/0.1.1'


[0.1.1] % git flow hotfix finish
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
Merge made by the 'recursive' strategy.
 README.md   | 2 --
 VERSION.txt | 2 +-
 2 files changed, 1 insertion(+), 3 deletions(-)
Switched to branch 'develop'
Merge made by the 'recursive' strategy.
 README.md   | 2 --
 VERSION.txt | 2 +-
 2 files changed, 1 insertion(+), 3 deletions(-)
To github.com:koide-g/git-flow-sandbox.git
 - [deleted]         hotfix/0.1.1
Deleted branch hotfix/0.1.1 (was ebe6300).

Summary of actions:
- Hotfix branch 'hotfix/0.1.1' has been merged into 'master'
- The hotfix was tagged 'v0.1.1'
- Hotfix tag 'v0.1.1' has been back-merged into 'develop'
- Hotfix branch 'hotfix/0.1.1' has been locally deleted; it has been remotely deleted from 'origin'
- You are now on branch 'develop'


[develop] % git tag
v0.1.0
v0.1.1


[develop] % git push origin master:master
Counting objects: 7, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 733 bytes | 733.00 KiB/s, done.
Total 7 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
To github.com:koide-g/git-flow-sandbox.git
   0432b2b..7c35828  master -> master

[develop] % git push origin v0.1.1
Total 0 (delta 0), reused 0 (delta 0)
To github.com:koide-g/git-flow-sandbox.git
 * [new tag]         v0.1.1 -> v0.1.1

[develop] % git push origin develop:develop
Counting objects: 1, done.
Writing objects: 100% (1/1), 233 bytes | 233.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0)
To github.com:koide-g/git-flow-sandbox.git
   335820e..6d0bba3  develop -> develop
```
