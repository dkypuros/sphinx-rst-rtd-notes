[< back home](README.md)

# 4. Documentation refinement: expanding our use or restructured text

**edit ".rst" files to start building sample restructured text files**

Let's edit **index.rst**

```rst
My documentation home page
============================

Sub heading. Fusce convallis ligula facilisis
---------------------------------------------
Arius urna vitae, rhoncus dolor. Fusce ipsum tellus, aliquam in **gravida** eget, venenatis non massa. Donec quis mi malesuada, porta lorem in, tristique ipsum. Integer ut elementum metus. https://www.google.com

* Vivamus nisl felis, iaculis in ante eu
* eleifend sodales enim. Vivamus id velit dictum
* ehicula velit


Sub heading. Fusce convallis ligula facilisis
---------------------------------------------
Arius urna vitae, rhoncus dolor. Fusce ipsum tellus, aliquam in gravida eget, venenatis non massa. Donec quis mi malesuada, porta lorem in, tristique ipsum. Integer ut elementum metus. Vivamus nisl felis, iaculis in ante eu, eleifend sodales enim. Vivamus id velit dictum, vehicula velit a, dapibus risus. Vivamus tempor viverra vehicula. https://www.google.com

1. Vivamus nisl felis, iaculis in ante eu
2. eleifend sodales enim. Vivamus id velit dictum
3. ehicula velit
```

**Because we have a link to an image let's create that folder and updload our image**

```bash
mkdir /images
```

Let's upload a silly ".png" file and grab the link.

```bash
https://github.com/dkypuros/openshift-lab-001/blob/main/images/ritz.png
```

***Now we can update the file above by embedding a link***

```rst
Sub heading. Fusce convallis ligula facilisis
---------------------------------------------
Arius urna vitae, rhoncus dolor. Fusce ipsum tellus, aliquam in gravida eget, venenatis non massa. Donec quis mi malesuada, porta lorem in, tristique ipsum. Integer ut elementum metus. Vivamus nisl felis, iaculis in ante eu, eleifend sodales enim. Vivamus id velit dictum, vehicula velit a, dapibus risus. Vivamus tempor viverra vehicula. https://www.google.com

.. figure:: /images/ritz.png
   :alt: Ritz for life image
   :scale: 80 %
   *Ritz is an italics type of snack*
   
```

Throughout this section, we can continually take a peak at the results here [https://openshift-lab-001.readthedocs.io/](https://openshift-lab-001.readthedocs.io/en/latest/)


Let's add a few pages as "sub pages" or lower than the index.rst file. You can also do this in VSCode too.

```bash
cd docs/source/
touch page1.rst
touch page2.rst
```

Now, go to vscode and paste the following code for page 1 and page 2. Note the top of the code, we've added a bookmark thingy to name the pages.

**page1**
```rst
.. _page1:

sub-page 1 
============================

Sub heading. Fusce convallis ligula facilisis
---------------------------------------------
Arius in **gravida** eget, venenatis non massa. Donec quis mi malesuada, porta lorem in, tristique ipsum. Integer ut elementum metus.

* Vivamus nisl felis, iaculis in ante eu
* eleifend sodales enim. Vivamus id velit dictum
* ehicula velit
```
**page2**
```rst
.. _page2:

sub-page 2 
============================

Sub heading. Fusce convallis ligula facilisis
---------------------------------------------
Arius in **gravida** eget, venenatis non massa. Donec quis mi malesuada, porta lorem in, tristique ipsum. Integer ut elementum metus.

* Vivamus nisl felis, iaculis in ante eu
* eleifend sodales enim. Vivamus id velit dictum
* ehicula velit

```

Now we can update our index.rst file to include a "toctree" or Table of Contents directive that references the file "page1.rst" and ":ref:" insertion that uses the bookmark like syntax at the top of the "page1.rst" file (aka .. _page1:)

Add this to the bottom of "index.rst"

```rst
My documentation home page
============================

Sub heading. Fusce convallis ligula facilisis
---------------------------------------------
Arius urna vitae, rhoncus dolor. Fusce ipsum tellus, aliquam in **gravida** eget, venenatis non massa. Donec quis mi malesuada, porta lorem in, tristique ipsum. Integer ut elementum metus. https://www.google.com

* :ref: <page1> Page 1 of the documentation is great.
* eleifend sodales enim. Vivamus id velit dictum
* ehicula velit


Sub heading. Fusce convallis ligula facilisis
---------------------------------------------
Arius urna vitae, rhoncus dolor. Fusce ipsum tellus, aliquam in gravida eget, venenatis non massa. Donec quis mi malesuada, porta lorem in, tristique ipsum. Integer ut elementum metus. Vivamus nisl felis, iaculis in ante eu, eleifend sodales enim. Vivamus id velit dictum, vehicula velit a, dapibus risus. Vivamus tempor viverra vehicula. https://www.google.com

.. figure:: /images/ritz.png
   :alt: Ritz for life image
   :scale: 80 %
   *Ritz is an italics type of snack*
   

1. Vivamus nisl felis, iaculis in ante eu
2. eleifend sodales enim. Vivamus id velit dictum
3. ehicula velit

.. toctree:: 
   :maxdepth: 2
   :caption: Contents:

   page1
```

Once these changes our made to our OpenShift repo, we can build new html pages, and push them to the GitHub repo.
(replace '1' with a comment)

To do a quick view locally:

```bash
make html
```
Continue to push updates to GitHub, and after 10 - 20 seconds ReadTheDocs.org will update via a webhook.

```bash
git add .
git commit -m "1"
git push
``


















