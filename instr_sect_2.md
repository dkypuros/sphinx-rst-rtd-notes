# Local dev and test: Create and build local environment (cloned folder)

[< back home](README.md)

**Python and virtual environment, PIP, Sphinx**

Check your versions of Python and PIP. 
```
python3 --version
pip --version
```

Let's make sure we're in the correct directory. Next install the **venv module** if it is not already installed. Next create a new virtual environment in a directory called **env** using the **venv module**. Finally activate the virtual environment using the **source** command.
```
cd /home/student/Documents/GitHub-files/openshift-lab-001
python3 -m pip install --user virtualenv
python3 -m venv env
source env/bin/activate
```

Once you are in your virtual environment (look for parenthesis on the far left of the command line) create a directory called **docs**. Next install the **Sphinx documentation generator** package via pip, the package installer for Python.
```
mkdir docs
cd docs
pip install sphinx
```

Now we can use the quickstart utility. We enter values and configure sphinx locally. 

```
sphinx-quickstart to initialize the directory structure.
```
I used the following values to configure sphinx.
```
>Separate source and build directories (y/n) [n]: y
>Project name: openshift-lab-001
> Author name(s): David Kypuros
> Project release []: 1
> Project language [en]: en
```
**Sphinx Quickstart** prints the following message to the screen once the values are set.
```
You should now populate your master file /Users/davidkypuros/Documents/GitHub-projects/openshift-lab-001/docs/source/index.rst and create other documentation
source files. Use the Makefile to build the docs, like so:
   make builder
where "builder" is one of the supported builders, e.g. html, latex or linkcheck.
```

So for me the command I will use from this summary is
```
make html
```
Take a look around and explore the new directory structure and files created during the **quickstart** process. Notice the two folders **build** and **source**. That's the seperation of the of the source and build directories we selected earlier in the process.

see output here and the image below:
```
Creating file /Users/davidkypuros/Documents/GitHub-projects/openshift-lab-001/docs/source/conf.py.
Creating file /Users/davidkypuros/Documents/GitHub-projects/openshift-lab-001/docs/source/index.rst.
Creating file /Users/davidkypuros/Documents/GitHub-projects/openshift-lab-001/docs/Makefile.
Creating file /Users/davidkypuros/Documents/GitHub-projects/openshift-lab-001/docs/make.bat.
```

![Directory Structure](https://github.com/dkypuros/sphinx-rst-rtd-notes/blob/main/images/new-sphinx-directory-structure.png "Structure")

**Exploring the 'homepage' for restructured text**

File located in "/docs/source/index.rst"

```rst
.. openshift-lab-001 documentation master file, created by
   sphinx-quickstart on Sat Feb 18 08:15:25 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to openshift-lab-001's documentation!
=============================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

```

Let's **change** the file by removing some of the "indices" and stuff. See the smaller file below:

```
.. openshift-lab-001 documentation master file, created by
   sphinx-quickstart on Sat Feb 18 08:15:25 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

David's documentation!
=============================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:
```

**Test vanilla build process (make)**

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tincidunt est at augue mattis, eu sagittis lectus iaculis. Praesent sit amet nibh ut diam tincidunt pellentesque vel eu ex. Sed in nulla tincidunt, pulvinar tellus et, euismod diam. 

**Test different HTML themes (included)**

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tincidunt est at augue mattis, eu sagittis lectus iaculis. Praesent sit amet nibh ut diam tincidunt pellentesque vel eu ex. Sed in nulla tincidunt, pulvinar tellus et, euismod diam. 

**Test customer HTML theme**

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tincidunt est at augue mattis, eu sagittis lectus iaculis. Praesent sit amet nibh ut diam tincidunt pellentesque vel eu ex. Sed in nulla tincidunt, pulvinar tellus et, euismod diam. 

**Create full restructured text document**

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tincidunt est at augue mattis, eu sagittis lectus iaculis. Praesent sit amet nibh ut diam tincidunt pellentesque vel eu ex. Sed in nulla tincidunt, pulvinar tellus et, euismod diam. 

**Review project locally**

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tincidunt est at augue mattis, eu sagittis lectus iaculis. Praesent sit amet nibh ut diam tincidunt pellentesque vel eu ex. Sed in nulla tincidunt, pulvinar tellus et, euismod diam. 
