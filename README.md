# Release repository for x86-generic-64

Montavista Software, LLC. release of x86-generic-64. 

How to use:
==========
```
git clone --recursive http://cgxcollective/cgx2.6/dev/msdbuilds/x86-generic-64-4.19-2.6/191003165342/x86-generic-64-4.19-2.6-cgx
cd x86-generic-64-4.19-2.6-cgx
source setup.sh
```
Optionally, you can pass setup.sh a directory name to use instead of the
default "project" as follows:

```
source setup.sh <project directory>
```
Note: If you are running setup.sh under another script, you should execute it
as a shell script:

```
bash setup.sh <project directory>
source <project directory>/setup.sh
```
The kernel sources by default will be checked out locally to the sources
directory. If you would rather have bitbake do the checkout run the following
command prior to sourcing setup.sh:

```
export LOCAL_SOURCES=0
```

After running the top level setup.sh, you are ready to build. When starting
another session, you can source the setup.sh script in the project directory
to get started. This script will automatically source the environment for
the build tools stored under buildtools, and sources the 
poky/oe-init-build-env script.

directory layout:
================
```
x86-generic-64-4.19-2.6-cgx/
       project - bitbake project for the x86-generic-64 project build
       buildtools - build tools to provide minimal build requirement for poky builds
       layers - layers for building x86-generic-64 project
       setup.sh - project setup script
       bin - various helper applications for setting up and maintaining the release directory
```

