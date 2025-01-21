# Environments

## Create new environment and switch to it

```bash
conda create -n name_of_new_env
conda activate name_of_new_env
```

Create environment with specific python version:

```bash
conda create -n name_of_new_env python 3.7
```

## Remove environment

```bash
conda remove -n name_of_env --all
# alternative: conda env remove -n name_of_env
```

## List all environments

```bash
conda env list
```

## Adding channels to environment

Activate the environment, then:

```bash
conda config --env --add channels conda-forge
```

## Sharing an environment

This can be useful if you want to document the package versions for a project or if you are collaborating with other people so they can work with the same environment.

```bash
conda env export > environment.yml
```

To exclude packages that were installed into the environment as a dependency add the flag `--from-history`.
This can help for cross-platform compatibility, because *conda* will figure out platform-specific dependencies.
However, this will not document the version of a package if the version was not explicitly stated when installing.

```bash
conda env export --from-history > environment.yml
```

To recreate the environment using the *yml* file:

```bash
conda env create -f environment.yml
```
