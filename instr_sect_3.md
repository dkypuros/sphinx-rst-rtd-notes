[< back home](README.md)

# 3. Documentation hosting: Publish documentation

**Upload local environment to GitHub (file hosting)**
These are the steps to publish your local sphinx site to ReadTheDocs.

**Ignore certain files**
Let's make sure the following was added to your "phython" gitignore file.

```bash
# Sphinx documentation
docs/_build/
```

**Go to `Readthedocs.org` and set the build up**

Visit the following site [readthedocs.org](https://readthedocs.org/) and [login](https://readthedocs.org/accounts/login/). Scroll down and select "sign in with GitHub". 

![Login Screen](https://github.com/dkypuros/sphinx-rst-rtd-notes/blob/main/images/read-the-docs-login.png "Login Screen")

Look for the following project and select the "plus sign" next to the repo path. Leave the defaults in the **Project Details** page and click **next**. 

```bash
dkypuros/openshift-lab-001
```

Here is what the next page should look like:

![Read The Docs Build Page](https://github.com/dkypuros/sphinx-rst-rtd-notes/blob/main/images/build.png "Read the Docs build page")

Now you're ready to select **build** to pull the docs from GitHub and publish them in ReadTheDocs.org. Once the build is complete, select "View Docs" in the top right corner of the build success page.

**Review the documentation on "Read The Docs"**

My page is now visable on ReadTheDoc's public hosting website.

[http://openshift-lab-001.readthedocs.io/](https://openshift-lab-001.readthedocs.io/en/latest/)

Here is a screenshot of the public site.

![Public Site](https://github.com/dkypuros/sphinx-rst-rtd-notes/blob/main/images/published-site-first-time.png)

