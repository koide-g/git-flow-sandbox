## git flow feature

```
[develop] % git flow feature start update-readme
Switched to a new branch 'feature/update-readme'

Summary of actions:
- A new branch 'feature/update-readme' was created, based on 'develop'
- You are now on branch 'feature/update-readme'

Now, start committing on your feature. When done, use:

     git flow feature finish update-readme

[update-readme] % vi README.md
On branch feature/update-readme
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (3a6dbedfb9d03b1ecb635c84e0aa455738c0206a)
  1 v0.1.0
[update-readme] % git commit -m readme++
On branch feature/update-readme
Changes not staged for commit:
	modified:   README.md

no changes added to commit
[update-readme] % git commit -am readme++
[feature/update-readme bef9ec3] readme++
 1 file changed, 11 insertions(+)


[update-readme] % git flow feature publish
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 311 bytes | 311.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:koide-g/git-flow-sandbox.git
 * [new branch]      feature/update-readme -> feature/update-readme
Branch 'feature/update-readme' set up to track remote branch 'feature/update-readme' from 'origin'.
Already on 'feature/update-readme'
Your branch is up to date with 'origin/feature/update-readme'.

Summary of actions:
- The remote branch 'feature/update-readme' was created or updated
- The local branch 'feature/update-readme' was configured to track the remote branch
- You are now on branch 'feature/update-readme'
  1 Merge branch 'release/0.1.0'


[update-readme] % git flow feature finish
Switched to branch 'develop'
Updating cb5887a..bef9ec3
Fast-forward
 README.md | 11 +++++++++++
 1 file changed, 11 insertions(+)
To github.com:koide-g/git-flow-sandbox.git
  1 0.1.0
 - [deleted]         feature/update-readme
  1 Merge tag 'v0.1.0' into develop
Deleted branch feature/update-readme (was bef9ec3).

Summary of actions:
- The feature branch 'feature/update-readme' was merged into 'develop'
- Feature branch 'feature/update-readme' has been locally deleted; it has been remotely deleted from 'origin'
- You are now on branch 'develop'
```
