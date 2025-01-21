# R, packages and its dependencies

## Installation

https://cloud.r-project.org/bin/linux/ubuntu/README.html

```bash
# adding secure apt key:
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9

# adding cran-mirror for Ubuntu 20.04:
sudo add-apt-repository 'deb https://cloud.r-project.org/bin/linux/ubuntu focal-cran40/'

# installing r-base and r-dev
sudo apt update
sudo apt install r-base r-base-dev
```

- RStudio: https://www.rstudio.com/products/rstudio/download/

## Dependencies of R packages

```bash
# "devtools":
sudo apt install libcurl4-openssl-dev libssl-dev libxml2-dev

#"rgl"
sudo apt install libcgal-dev libglu1-mesa-dev libglu1-mesa-dev libfreetype6-dev

# "rattle":
sudo apt install libcanberra-gtk-module
sudo apt install wajig
wajig install libgtk2.0-dev libxml2-dev

# "cairo":
sudo apt-get install libcairo2-dev

# "sbrl"
sudo apt install libgsl-dev
```

## RWeka:

```bash
java –version

sudo apt install default-jre default-jdk

javac -version
```

## Archive:

- https://www.r-bloggers.com/why-is-r-slow-some-explanations-and-mklopenblas-setup-to-try-to-fix-this/
