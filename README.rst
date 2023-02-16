Playground for learning the following technologies
===================================================

.. contents:: Overview

#. Sphinx
#. Restructured Text (feature rich Markdown type syntax)
#. ReadTheDocs.org (open source documents hosting website)

The Purpose for Learning
--------------------------

My goal originally was to understand the foundational components of building an "environment" that is needed to deploy and manage Red Hat OpenShift. Keep in mind there are many deployment scenarios for OpenShift. 

    - User Provisioned Infrastructure (UPI)
    - Installer Provisioned Infrastructure (IPI)
    - Assisted Service Installer frrom console.redhat.com
    - Agent-based Installer (magic ISO)

They all have one thing in common. They need an environment. 

So in the pursuit of learning more about this pre-requisite environment, I discovered the importance of documenting the many many layer of the configuration in a way that I can come back to, and reference my personal documentation. It's a lot to remember! This led to my desire to learn the following:

    - Sphinx
    - ReStructured Text
    - ReadTheDocs.org

The goal is to have a "Pocket Guide" of sorts that will help me save time in the future.

Before starting
++++++++++++++++

There are (2) repositories

This will be my place to take notes on how to document with Sphinx. (1) This repository is called "sphinx-rst-rtd-notes". Keep in mind I will setup (2) another repository to actually create a sample sphinx project. This actual project repo is called "openshift-lab-001"

Sphinx Training Materials from Audrey

https://techwritingmatters.com/documenting-with-sphinx-tutorial-intro-overview


Part 1 - GitHub
-----------------
Setup the a github repository to store project files. This is an easy step, so I'm not including many details.

    - Setup new GitHub repo 
    - clone locally
    - add README.rst
  
Completed! 

https://github.com/dkypuros/openshift-lab-001


Part 2 - Python & PIP
-----------------------
setup a local environment to generate the documentation.


Python Setup
+++++++++++++

These should be installed (I'm using Pythong3)

```
python --version
pip --version
python3 -m pip install --user virtualenv
cd /home/student/Documents/GitHub-files/openshift-lab-001
python3 -m venv env
source env/bin/activate
```