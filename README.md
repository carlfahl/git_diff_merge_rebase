# Git Workshop on Diff, Merge, and Rebase

### Step 1: Create branches, show diffs and merge.

* Create a new git repo, Add README.md and index.html file (default atom html snippet).
* Add, commit and push these changes to github.
* run `git log` to see the new commit in the history.  run `git status` and `git diff` to see that there are not changes in your working dir.
* Create a topic branch `git branch new_feature` then `git checkout new_feature`.  This creates a new branch and makes it your working branch.
`git checkout -b new_feature` is a short cut that is equivalent to running both commands.
* run `git branch` to see the branches.  The `*` is the active branch.
* run `git log --all --graph --decorate --oneline`.  (make an alias to this command - mine is `gitg`) This shows all commits in all the branches and
label the branches and the HEAD.
* create `css/style.css` and add content then run `git diff`.  Notice that style.css is not in the diff.  Only tracked files are in the diff.
* run `git add -A` and `git diff`.  Notice that there is still no output.  Run `git diff --staged` this shows staged changes.
* add and commit changes.
* run `gitg` (Or what you named the alias).  Output should look like this:

```
* 247c577 (HEAD -> new_feature) Readme updates and added css/style.css
* d9a638e (master) update to readme
* 26988b1 (origin/master) Initial commit of README and index on branch master
```
* run `git checkout master` to change back to the master branch.  run `git merge new_feature` to bring the changes in from the new_feature branch.
* `gitg` still shows a linear series of changes.
* edit the index.html file in the master branch; switch to the new_feature branch; edit the same lines in the new_feature branch.
* commit these changes to the new_feature branch.
* `gitg` now shows diverging branches.  Note that the HEAD is the most recent commit on new_feature.
* `git checkout master`.  Now the HEAD is now the most recent commit on master.


### Step 2:
