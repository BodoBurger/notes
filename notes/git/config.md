# Setup and Config

## `config`

### Show or change Git username or email address

```Bash
$ git config --list # repository-specific settings
$ git config --list --global # global git settings
$ git config user.name "Enrico Pallazzo"
$ git config user.email "enrico.pallazzo@lapd.com"
```
The global settings are stored in the Git config file
in the HOME directory (`~/.gitconfig`),
repository-specific settings are found at `.git/config`
in the respective repository folder.
