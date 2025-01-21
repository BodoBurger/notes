# Basics

## `rm`

### Remove files from the index without removing them from disc

If you forgot to add a file to `.gitignore`:

```Bash
$ git rm -rf --cached file-name
```

The file is now untracked and can be added to `.gitignore`.
Then, you can commit the deletion and the modified gitignore file.
