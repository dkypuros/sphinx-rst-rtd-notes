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


