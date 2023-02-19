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

Let's **change** the file by removing some of the "indices" and adding some "Lorem Ipsum" placeholder text. See the smaller file below:

```rst
David's documentation!
=============================================

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris mattis tempus ex, eget posuere orci fringilla ac. Vivamus sagittis eget diam sit amet varius. Cras ligula odio, aliquam consectetur tellus ac, porttitor porttitor massa. Proin mi risus, facilisis ut varius eget, aliquet a lacus. Vestibulum et augue justo. Pellentesque a lorem ex. Nulla facilisis, nisl eu vehicula semper, ex mi aliquet est, in rutrum dolor ex et dolor.

.. toctree::
   :maxdepth: 2
   :caption: Contents:
```

**Test vanilla build process (make)**

Initiate the **make** process to allow Sphinx to build all of the html files.

```bash
make html
```
Here is the what the output should look like:

![Make](https://github.com/dkypuros/sphinx-rst-rtd-notes/blob/main/images/make.png "Make HTML command")

After making minor changes to the **index.rst** and running **make html** we can simple website consisting of one HTML file. Notice, even with onlh one page, the website is fully searchable. Search for **David** in the search box. It works!

![HTML](https://github.com/dkypuros/sphinx-rst-rtd-notes/blob/main/images/first-html.png "Simple HTML page")

**Test the included HTML themes)**

Check the sphinx website to review options for **themes**. Let's focus on the themes included with Sphinx first.

[Sphinx HTML Theme Website ⊂(◉‿◉)つ ](https://www.sphinx-doc.org/en/master/usage/theming.html)

Get the name of the included theme, and open up the **conf.py**. Change the bottom of the **conf.py** file to match the following text below:

```bash
html_theme = 'classic'
html_static_path = ['_static']

html_theme_options = {
    "rightsidebar": "true",
    "relbarbgcolor": "black"
}
```


**Test customer HTML theme**

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tincidunt est at augue mattis, eu sagittis lectus iaculis. Praesent sit amet nibh ut diam tincidunt pellentesque vel eu ex. Sed in nulla tincidunt, pulvinar tellus et, euismod diam. 

**Create full restructured text document**

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tincidunt est at augue mattis, eu sagittis lectus iaculis. Praesent sit amet nibh ut diam tincidunt pellentesque vel eu ex. Sed in nulla tincidunt, pulvinar tellus et, euismod diam. 

**Review project locally**

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tincidunt est at augue mattis, eu sagittis lectus iaculis. Praesent sit amet nibh ut diam tincidunt pellentesque vel eu ex. Sed in nulla tincidunt, pulvinar tellus et, euismod diam. 
