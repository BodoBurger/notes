# Conda

[Conda](https://conda.io) is a package manager and environment management system.

## Resources

- [Conda docs](https://conda.io/projects/conda)
- [Conda cheat sheet](https://conda.io/projects/conda/en/latest/user-guide/cheatsheet.html)
- [Conda: Myths and Misconceptions](https://jakevdp.github.io/blog/2016/08/25/conda-myths-and-misconceptions/)
- [Conda forge (an alternative distribution for conda)](https://conda-forge.org/)


## Installation

- [Installing Miniconda](https://docs.anaconda.com/miniconda/install/)
- [Installing Anaconda](https://docs.anaconda.com/anaconda/install/linux/)
- [Uninstall](https://docs.anaconda.com/anaconda/uninstall/)


### Miniforge

https://conda-forge.org/download/

```bash
bash Miniforge3-Linux-x86_64.sh
```

### Miniconda

```bash
# Download
curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

# Installation
bash ~/Miniconda3-latest-Linux-x86_64.sh

# Activate
source ~/.bashrc
```

### Should you add Conda to the PATH?

- [Conda FAQ](https://docs.anaconda.com/working-with-conda/reference/faq/)


#### Prevent conda from activating the base env by default

- [Stackoverflow Thread](https://stackoverflow.com/questions/54429210/how-do-i-prevent-conda-from-activating-the-base-environment-by-default)

```bash
conda config --set auto_activate_base false
```


### Want to change kernel in jupyter?

Base environment needs the `nb_conda_kernels` package.
Every environment needs the ipykernel package.

```bash
conda install nb_conda_kernels
```

## Archived

### Deep learning environment

Prereq:

```bash
sudo apt-get install libhdf5-serial-dev # for saving keras models efficiently

sudo apt install graphviz
```

```bash
conda create -n deeplearn
source activate deeplearn

conda install tensorflow-gpu

conda install matplotlib
conda install opencv # needed for some examples
conda install pydot # graphviz
conda install pillow # python imaging library

conda install cython # Why?

conda install ipykernel # for kernel selection in jupyter

# conda install matplotlib PyYAML opencv-python pydot pillow cython
```

### Check tensorflow gpu

```python
import tensorflow as tf
tf.test.is_gpu_available(
    cuda_only=False,
    min_cuda_compute_capability=None
)
```

- [Install TensorFlow with GPU Support the Easy Way](https://www.pugetsystems.com/labs/hpc/Install-TensorFlow-with-GPU-Support-the-Easy-Way-on-Ubuntu-18-04-without-installing-CUDA-1170/)
