# Sharing and Updating Projects


## Remote

https://git-scm.com/docs/git-remote

### Push local repository to existing remote

```Bash
$ git remote add origin git@github.com:USERNAME/REPOSITORY.git
$ git push --all --set-upstream origin
```

### Show or change remote

In this example we switch from HTTPS to SSH:

```Bash
$ git remote -v
> origin  https://github.com/USERNAME/REPOSITORY.git (fetch)
> origin  https://github.com/USERNAME/REPOSITORY.git (push)
$ git remote set-url origin git@github.com:USERNAME/REPOSITORY.git
$ git remote -v
> origin  git@github.com:USERNAME/REPOSITORY.git (fetch)
> origin  git@github.com:USERNAME/REPOSITORY.git (push)
```

## Submodules

https://git-scm.com/docs/git-submodule

### Add a submodule

```Bash
git submodule add git@github.com:USERNAME/REPOSITORY.git PATH/TO/SUBMODULEDIR
```

### Download files to empty submodule directory

When cloning a repository with submodules and the submodule directories are empty:

```Bash
git submodule update --init --recursive
```

### Remove a submodule (leaving no trace)

```Bash
git rm PATH/TO/SUBMODULEDIR
rm -rf .git/modules/PATH/TO/SUBMODULEDIR
git config -f .git/config --remove-section submodule.PATH/TO/SUBMODULEDIR 2> /dev/null
```
