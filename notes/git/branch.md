# Branching and Merging

## Branches

### Change branch without committing changes: stash and pop

Want to have a look at another branch without committing changes done so far?
Put them in a stash where they can hide until you switch back.

```Bash
$ git stash # on the original branch
$ git checkout other-branch
# do some stuff on the other branch
$ git checkout original-branch
$ git stash pop
```

More about [*git-stash*](https://git-scm.com/docs/git-stash).

### Create a local branch, push it to a remote repository and track it

```Bash
$ git checkout -b MyNewBranch # create and switch to new branch
# do some stuff
$ git push -u origin MyNewBranch
```

### Delete local branch

```Bash
$ git branch -d MyLocalBranch
```

## Merging

### Merge master into feature branch before making a PR

```Bash
$ git checkout master
$ git pull
$ git checkout new-feature
$ git add *files-and-changes*
$ git commit -m "feature description"
$ git reset HEAD --hard # removes all uncommited files
$ rm *untracked-files*  # to prevent merge conflicts
$ git merge master
# resolve potential merge conflicts
$ git commit -m "resolved mergeconflicts | merged master"
$ git push origin new-feature
```
