# Project background and description

[< back home](README.md)

### About the project | Why work on this?

**The Purpose for Learning**

My goal originally was to understand the foundational components of building an "environment" that is needed to deploy and manage Red Hat OpenShift. Keep in mind there are many deployment scenarios for OpenShift. 

- User Provisioned Infrastructure (UPI)
- Installer Provisioned Infrastructure (IPI)
- Assisted Installer from console.redhat.com
- Agent-based Installer (magic ISO)

They all have one thing in common. They need an environment. When I say environment, I mean routing and linux networking services such as DNS/DDNS, DHCP and Directory Services like IdM (DDD). Each of these services needs care and feeding, integration testing and tooling for troubleshooting. 

So in the pursuit of learning more about this pre-requisite environment, I discovered the importance of documenting this "pre-environment" before digging deeper into Red Hat OCP. 

So, a "sub-goal" then is to sharpen my documentatin skills, and my linux DDD skills in such a way that I can come back this when things aren't working correctly in OpenShift. 

**So my sub-goal is to learn the following documentation tools:**

- Sphinx
- ReStructured Text
- ReadTheDocs.org

### About the project | Description of the technology

**The Technology**

We'll use git to host files. We'll use **Python** version 3 and **pip** to install **Sphinx** (free and open-source documentation generation tool). We'll use **reStructuredText** as a markup language. Sphinx will use this markup to create the documentation, and it output the documentation in HTML.

As a small note: Sphinx is widely used in the Python community and is a powerful tool for creating high-quality documentation for projects of all sizes.

### About the project | Project Flow

**Project Flow and Diagram**

Starting from the **LEFT** Initially we're going to setup our local system to use GitHub as a file repository for our documentation files. On the **BOTTOM** we'll work on our files, review them locally. Once we're ready to publish them publically to see what our project will look like ont he web **RIGHT** we'll setup "readthedocs.org" to pull our files from GitHub and build a mini documentation website accordingly.

![Architectural Flow](https://github.com/dkypuros/sphinx-rst-rtd-notes/blob/main/images/architectural-flows.png "Flows")
