# Install R version 3.4.4 on Ubuntu notes.

This is proved work on Ubuntu 17 OS.

### Install all dependencies
If you don't have compiler 77 on your machine, well usually you don't have...
```
sudo apt-get install gfortran
```
then
```
sudo apt-get install build-essential
sudo apt-get install fort77
sudo apt-get install xorg-dev
sudo apt-get install liblzma-dev  libblas-dev gfortran
sudo apt-get install gcc-multilib
sudo apt-get install gobjc++
sudo apt-get install aptitude
sudo aptitude install libreadline-dev
sudo aptitude install libcurl4-openssl-dev
sudo apt-get install default-jdk
sudo apt-get install texlive-latex-base
sudo apt-get install libcairo2-dev 
```
### Install r-base with ubuntu
```
sudo apt-get install r-base
```
### Install newest version of R from source
```
 wget https://cran.r-project.org/src/base/R-3/R-3.4.4.tar.gz
./configure --prefix=/home/jtrembla/software/R/R-3.4.4 --with-x=yes --enable-R-shlib=yes --with-cairo=yes
make
```
### IF NEWS.pdf file is missing and will make installation crash.
```
touch doc/NEWS.pdf
```

### Let's make.
```
make install
```

### Update PATH
```
export PATH=~/software/R/R-3.4.4/bin:$PATH
export RSTUDIO_WHICH_R=~/software/R/R-3.4.4/bin/R
```

### Problem when you try to install pacman and get this error:
```
no Package called pacman
```

or 
```
ERROR: configuration failed for package ‘git2r’
* removing ‘/usr/local/lib/R/site-library/git2r’
Warning in install.packages :
  installation of package ‘git2r’ had non-zero exit status
ERROR: dependency ‘git2r’ is not available for package ‘devtools’
* removing ‘/usr/local/lib/R/site-library/devtools’
Warning in install.packages :
  installation of package ‘devtools’ had non-zero exit status

```
use:
```
sudo apt-get install ssllib-dev
```
### Acknowledgements
A lot of thanks to [Jtremblay](https://github.com/jtremblay) and his work [this article](http://jtremblay.github.io/software_installation/2017/06/21/Install-R-3.4.0-and-RStudio-on-Ubuntu-16.04), which saved me a lot of time to build the R environment.
