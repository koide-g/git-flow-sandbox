## git flow release

```
[develop] % git flow release start 0.1.0
Switched to a new branch 'release/0.1.0'

Summary of actions:
- A new branch 'release/0.1.0' was created, based on 'develop'
- You are now on branch 'release/0.1.0'

Follow-up actions:
- Bump the version number now!
- Start committing last-minute fixes in preparing your release
- When done, run:

     git flow release finish '0.1.0'

[0.1.0] % vi VERSION.txt
[0.1.0] % git add .
[0.1.0] % git commit -m 'bump v0.1.0'
[release/0.1.0 2347387] bump v0.1.0
 1 file changed, 1 insertion(+)
 create mode 100644 VERSION.txt
 
 
[0.1.0] % git flow release publish
Counting objects: 6, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 557 bytes | 557.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0)
To github.com:koide-g/git-flow-sandbox.git
 * [new branch]      release/0.1.0 -> release/0.1.0
Branch 'release/0.1.0' set up to track remote branch 'release/0.1.0' from 'origin'.
Already on 'release/0.1.0'
Your branch is up to date with 'origin/release/0.1.0'.

Summary of actions:
- The remote branch 'release/0.1.0' was created or updated
- The local branch 'release/0.1.0' was configured to track the remote branch
- You are now on branch 'release/0.1.0'

[0.1.0] % git flow release finish
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
Merge made by the 'recursive' strategy.
 README.md   | 11 +++++++++++
 VERSION.txt |  1 +
 2 files changed, 12 insertions(+)
 create mode 100644 VERSION.txt
Already on 'master'
Your branch is ahead of 'origin/master' by 3 commits.
  (use "git push" to publish your local commits)
Switched to branch 'develop'
Merge made by the 'recursive' strategy.
 VERSION.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 VERSION.txt
To github.com:koide-g/git-flow-sandbox.git
 - [deleted]         release/0.1.0
Deleted branch release/0.1.0 (was 2347387).

Summary of actions:
- Release branch 'release/0.1.0' has been merged into 'master'
- The release was tagged 'v0.1.0'
- Release tag 'v0.1.0' has been back-merged into 'develop'
- Release branch 'release/0.1.0' has been locally deleted; it has been remotely deleted from 'origin'
- You are now on branch 'develop'


[develop] % git push origin develop:develop
Counting objects: 8, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (6/6), done.
  1 Merge branch 'hotfix/v0.1.1'
Writing objects: 100% (8/8), 796 bytes | 796.00 KiB/s, done.
Total 8 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), done.
To github.com:koide-g/git-flow-sandbox.git
  1 hotfix 0.1.1
 * [new branch]      develop -> develop
  1 Merge tag 'v0.1.1' into develop

[develop] % git push origin master:master
Total 0 (delta 0), reused 0 (delta 0)
To github.com:koide-g/git-flow-sandbox.git
   cb5887a..0432b2b  master -> master

[develop] % git push origin v0.1.0
Counting objects: 1, done.
Writing objects: 100% (1/1), 150 bytes | 150.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0)
To github.com:koide-g/git-flow-sandbox.git
 * [new tag]         v0.1.0 -> v0.1.0
```

