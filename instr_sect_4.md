[< back home](README.md)

# 4. Documentation refinement: expanding our use or restructured text

**edit ".rst" files to start building sample restructured text files**

Let's updater the **index.rst**

```rst
My documentation home page
============================

Example Sub heading
---------------------------------------------
Arius **gravida** eget, venenatis non massa. Donec quis mi. Integer ut elementum metus. https://www.google.com

* item 1
* item 2

.. figure:: images/ritz.png
      :alt: Ritz for life image
      :scale: 40 %

.. toctree:: 
   :maxdepth: 2
   :caption: Table of Contents:
   
   page1
   page2
```

**Let's go back and add the ritz image**

Create a folder in the "source" folder for images. Keep in mind this folder gets copied to the "docs/build/html/_images" area via "make html".

```bash
mkdir /docs/source/images
```

Grab a silly ".png" file and place it in the folder. I used this [photo](![image](https://user-images.githubusercontent.com/363856/220183710-8210386e-ff97-49d0-bcca-7c18c92d6c36.png)
) Make sure it's in the correct folder. See below.

```bash
/docs/source/images/ritz.png
```
**View the new "index.rst"**

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
.. _Section1:

Section 1
============================

Creating a mindmap
---------------------------------------------
Arius in **gravida** eget, venenatis non massa. Donec quis mi malesuada, porta lorem in, tristique ipsum. Integer ut elementum metus.

* Vivamus nisl felis, iaculis in ante eu
* eleifend sodales enim. Vivamus id velit dictum
* ehicula velit

Moving toward a new vision
---------------------------------------------
Arius urna vitae, rhoncus dolor. Fusce ipsum tellus, aliquam in gravida eget

Now that we've finished here click next to continue ore click here, :ref:`My Personal Map <section2>` to start developing your map.
```


**page2**
```rst
.. _Section2:

Section 2
============================

Now where do develop the map
---------------------------------------------
Arius in **gravida** eget, venenatis non massa. Donec quis mi malesuada, porta lorem in, tristique ipsum. Integer ut elementum metus.

* Vivamus nisl felis, iaculis in ante eu
* eleifend sodales enim. Vivamus id velit dictum
* ehicula velit

Practice excercises
---------------------------------------------
Arius urna vitae, rhoncus dolor. Fusce ipsum tellus, aliquam in gravida eget,
```

**These are the quick steps to iterate locally and publish to RTD**

Once these changes our made to our OpenShift repo, we can build new html pages, and push them to the GitHub repo.
(replace '1' with a comment)

To do a quick view locally (this will differ if you have multiple systems your using to test/dev). You might need to refresh the page a few time, or click the main link in the top left "openshift-lab-001" (above the search docs) area.

```bash
make html
```
Continue to push updates to GitHub, and after 10 - 20 seconds ReadTheDocs.org will update via a webhook.

```bash
git add .
git commit -m "1"
git push
```


**Here are a final set of files to show reST syntax**

```rst
My documentation home page
============================

Example Sub heading
---------------------------------------------
Arius **gravida** eget, venenatis non massa. Donec quis mi. Integer ut elementum metus. https://www.google.com

* item 1
* item 2

.. figure:: images/ritz.png
      :alt: Ritz for life image
      :scale: 40 %

.. toctree:: 
   :maxdepth: 2
   :caption: Table of Contents:
   
   page1
   page2
```

**page 1**

```rst
.. _Section1:

Section 1
============================

Creating a mindmap
---------------------------------------------
Arius in **gravida** eget, venenatis non massa. Donec quis mi malesuada, porta lorem in, tristique ipsum. Integer ut elementum metus.

* Vivamus nisl felis, iaculis in ante eu
* eleifend sodales enim. Vivamus id velit dictum
* ehicula velit

Moving toward a new vision
---------------------------------------------
Arius urna vitae, rhoncus dolor. Fusce **new button** |newbutton| tellus, aliquam in gravida eget

.. |newbutton| image:: images/ritz.png
               :scale: 10 %

Now that we've finished here click next to continue ore click here, :ref:`My Personal Map <section2>` to start developing your map.

Don't forget about the .. :ref:`practice excercises section! <practice>`
```

**page 2**

``rst
.. _Section2:

Section 2
============================

Now where do develop the map
---------------------------------------------
Arius in **gravida** eget, venenatis non massa. Donec quis mi malesuada, porta lorem in, tristique ipsum. Integer ut elementum metus.

* Vivamus nisl felis, iaculis in ante eu
* eleifend sodales enim. Vivamus id velit dictum
* ehicula velit

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc non arcu tellus. Praesent volutpat magna eget ipsum hendrerit, et vulputate ligula ullamcorper. Mauris pretium leo vitae odio efficitur feugiat. Suspendisse sed orci posuere, laoreet libero quis, ultricies est. Nullam accumsan faucibus placerat. Nunc a tempor neque, eget luctus nisi. Praesent aliquam urna magna, at elementum arcu sollicitudin sollicitudin. Morbi malesuada, elit nec faucibus dictum, leo nibh dapibus nulla, a hendrerit tellus mi fringilla dui. Duis iaculis justo a ante aliquam porta ut sed nunc. Nullam non felis urna. Phasellus vitae ornare ligula. Nam tellus lorem, accumsan eget erat ac, laoreet facilisis odio. Proin et dignissim lacus, at feugiat diam. Aenean nec sapien felis. Ut lorem ex, finibus id justo vitae, dictum pulvinar felis. Quisque volutpat ligula elementum, tempor massa vitae, facilisis massa.



.. tip:: 

   Tip statement. Remember! Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc non arcu tellus. Praesent volutpat magna eget ipsum hendrerit, et vulputate ligula ullamcorper. Mauris pretium leo vitae odio efficitur feugiat. Thank you.


HJK neque odio, fringilla vitae risus non, ornare vehicula tortor. Phasellus ultricies rhoncus lacus ac tempor. Quisque viverra molestie molestie. Etiam volutpat mauris pulvinar tellus varius molestie. Donec tortor arcu, elementum vitae mauris quis, rutrum finibus ante. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Nulla nibh quam, vulputate et ex ut, lobortis tristique neque.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc non arcu tellus. Praesent volutpat magna eget ipsum hendrerit, et vulputate ligula ullamcorper. Mauris pretium leo vitae odio efficitur feugiat. Suspendisse sed orci posuere, laoreet libero quis, ultricies est. Nullam accumsan faucibus placerat. Nunc a tempor neque, eget luctus nisi. Praesent aliquam urna magna, at elementum arcu sollicitudin sollicitudin. Morbi malesuada, elit nec faucibus dictum, leo nibh dapibus nulla, a hendrerit tellus mi fringilla dui. Duis iaculis justo a ante aliquam porta ut sed nunc. Nullam non felis urna. Phasellus vitae ornare ligula. Nam tellus lorem, accumsan eget erat ac, laoreet facilisis odio. Proin et dignissim lacus, at feugiat diam. Aenean nec sapien felis. Ut lorem ex, finibus id justo vitae, dictum pulvinar felis. Quisque volutpat ligula elementum, tempor massa vitae, facilisis massa.

Cras neque odio, fringilla vitae risus non, ornare vehicula tortor. Phasellus ultricies rhoncus lacus ac tempor. Quisque viverra molestie molestie. Etiam volutpat mauris pulvinar tellus varius molestie. Donec tortor arcu, elementum vitae mauris quis, rutrum finibus ante. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Nulla nibh quam, vulputate et ex ut, lobortis tristique neque.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc non arcu tellus. Praesent volutpat magna eget ipsum hendrerit, et vulputate ligula ullamcorper. Mauris pretium leo vitae odio efficitur feugiat. Suspendisse sed orci posuere, laoreet libero quis, ultricies est. Nullam accumsan faucibus placerat. Nunc a tempor neque, eget luctus nisi. Praesent aliquam urna magna, at elementum arcu sollicitudin sollicitudin. Morbi malesuada, elit nec faucibus dictum, leo nibh dapibus nulla, a hendrerit tellus mi fringilla dui. Duis iaculis justo a ante aliquam porta ut sed nunc. Nullam non felis urna. Phasellus vitae ornare ligula. Nam tellus lorem, accumsan eget erat ac, laoreet facilisis odio. Proin et dignissim lacus, at feugiat diam. Aenean nec sapien felis. Ut lorem ex, finibus id justo vitae, dictum pulvinar felis. Quisque volutpat ligula elementum, tempor massa vitae, facilisis massa.

Cras neque odio, fringilla vitae risus non, ornare vehicula tortor. Phasellus ultricies rhoncus lacus ac tempor. Quisque viverra molestie molestie. Etiam volutpat mauris pulvinar tellus varius molestie. Donec tortor arcu, elementum vitae mauris quis, rutrum finibus ante. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Nulla nibh quam, vulputate et ex ut, lobortis tristique neque.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc non arcu tellus. Praesent volutpat magna eget ipsum hendrerit, et vulputate ligula ullamcorper. Mauris pretium leo vitae odio efficitur feugiat. Suspendisse sed orci posuere, laoreet libero quis, ultricies est. Nullam accumsan faucibus placerat. Nunc a tempor neque, eget luctus nisi. Praesent aliquam urna magna, at elementum arcu sollicitudin sollicitudin. Morbi malesuada, elit nec faucibus dictum, leo nibh dapibus nulla, a hendrerit tellus mi fringilla dui. Duis iaculis justo a ante aliquam porta ut sed nunc. Nullam non felis urna. Phasellus vitae ornare ligula. Nam tellus lorem, accumsan eget erat ac, laoreet facilisis odio. Proin et dignissim lacus, at feugiat diam. Aenean nec sapien felis. Ut lorem ex, finibus id justo vitae, dictum pulvinar felis. Quisque volutpat ligula elementum, tempor massa vitae, facilisis massa.

Cras neque odio, fringilla vitae risus non, ornare vehicula tortor. Phasellus ultricies rhoncus lacus ac tempor. Quisque viverra molestie molestie. Etiam volutpat mauris pulvinar tellus varius molestie. Donec tortor arcu, elementum vitae mauris quis, rutrum finibus ante. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Nulla nibh quam, vulputate et ex ut, lobortis tristique neque.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc non arcu tellus. Praesent volutpat magna eget ipsum hendrerit, et vulputate ligula ullamcorper. Mauris pretium leo vitae odio efficitur feugiat. Suspendisse sed orci posuere, laoreet libero quis, ultricies est. Nullam accumsan faucibus placerat. Nunc a tempor neque, eget luctus nisi. Praesent aliquam urna magna, at elementum arcu sollicitudin sollicitudin. Morbi malesuada, elit nec faucibus dictum, leo nibh dapibus nulla, a hendrerit tellus mi fringilla dui. Duis iaculis justo a ante aliquam porta ut sed nunc. Nullam non felis urna. Phasellus vitae ornare ligula. Nam tellus lorem, accumsan eget erat ac, laoreet facilisis odio. Proin et dignissim lacus, at feugiat diam. Aenean nec sapien felis. Ut lorem ex, finibus id justo vitae, dictum pulvinar felis. Quisque volutpat ligula elementum, tempor massa vitae, facilisis massa.

Cras neque odio, fringilla vitae risus non, ornare vehicula tortor. Phasellus ultricies rhoncus lacus ac tempor. Quisque viverra molestie molestie. Etiam volutpat mauris pulvinar tellus varius molestie. Donec tortor arcu, elementum vitae mauris quis, rutrum finibus ante. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Nulla nibh quam, vulputate et ex ut, lobortis tristique neque.

.. _practice:

Practice excercises
---------------------------------------------
Arius urna vitae, rhoncus dolor. Fusce ipsum tellus, aliquam in gravida eget.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc non arcu tellus. Praesent volutpat magna eget ipsum hendrerit, et vulputate ligula ullamcorper. Mauris pretium leo vitae odio efficitur feugiat. Suspendisse sed orci posuere, laoreet libero quis, ultricies est. Nullam accumsan faucibus placerat. Nunc a tempor neque, eget luctus nisi. Praesent aliquam urna magna, at elementum arcu sollicitudin sollicitudin. Morbi malesuada, elit nec faucibus dictum, leo nibh dapibus nulla, a hendrerit tellus mi fringilla dui. Duis iaculis justo a ante aliquam porta ut sed nunc. Nullam non felis urna. Phasellus vitae ornare ligula. Nam tellus lorem, accumsan eget erat ac, laoreet facilisis odio. Proin et dignissim lacus, at feugiat diam. Aenean nec sapien felis. Ut lorem ex, finibus id justo vitae, dictum pulvinar felis. Quisque volutpat ligula elementum, tempor massa vitae, facilisis massa.

.. warning::

   Warning. Cras neque odio, fringilla vitae risus non, ornare vehicula tortor. 
   
.. DANGER::
   Beware killer rabbits!

.. admonition:: And, by the way...

   You can make up your own admonition too.

Suspendisse sed orci posuere, laoreet libero quis, ultricies est. Nullam accumsan faucibus placerat. Nunc a tempor neque, eget luctus nisi. Praesent aliquam urna magna, at elementum arcu sollicitudin sollicitudin. Morbi malesuada, elit nec faucibus dictum, leo nibh dapibus nulla, a hendrerit tellus mi fringilla dui. Duis iaculis justo a ante aliquam porta ut sed nunc. Nullam non felis urna. Phasellus vitae ornare ligula. Nam tellus lorem, accumsan eget erat ac, laoreet facilisis odio. Proin et dignissim lacus, at feugiat diam. Aenean nec sapien felis. Ut lorem ex, finibus id justo vitae, dictum pulvinar felis. Quisque volutpat ligula elementum, tempor massa vitae, facilisis massa.

Cras neque odio, fringilla vitae risus non, ornare vehicula tortor. Phasellus ultricies rhoncus lacus ac tempor. Quisque viverra molestie molestie. Etiam volutpat mauris pulvinar tellus varius molestie. Donec tortor arcu, elementum vitae mauris quis, rutrum finibus ante. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Nulla nibh quam, vulputate et ex ut, lobortis tristique neque.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc non arcu tellus. Praesent volutpat magna eget ipsum hendrerit, et vulputate ligula ullamcorper. Mauris pretium leo vitae odio efficitur feugiat. Suspendisse sed orci posuere, laoreet libero quis, ultricies est. Nullam accumsan faucibus placerat. Nunc a tempor neque, eget luctus nisi. Praesent aliquam urna magna, at elementum arcu sollicitudin sollicitudin. Morbi malesuada, elit nec faucibus dictum, leo nibh dapibus nulla, a hendrerit tellus mi fringilla dui. Duis iaculis justo a ante aliquam porta ut sed nunc. Nullam non felis urna. Phasellus vitae ornare ligula. Nam tellus lorem, accumsan eget erat ac, laoreet facilisis odio. Proin et dignissim lacus, at feugiat diam. Aenean nec sapien felis. Ut lorem ex, finibus id justo vitae, dictum pulvinar felis. Quisque volutpat ligula elementum, tempor massa vitae, facilisis massa.

Cras neque odio, fringilla vitae risus non, ornare vehicula tortor. Phasellus ultricies rhoncus lacus ac tempor. Quisque viverra molestie molestie. Etiam volutpat mauris pulvinar tellus varius molestie. Donec tortor arcu, elementum vitae mauris quis, rutrum finibus ante. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Nulla nibh quam, vulputate et ex ut, lobortis tristique neque.
```

