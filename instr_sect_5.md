Special section for using GitHub CodeSpaces

..code-block:: bash
  python3 --version
  pip --version

..code-block:: bash
  cd sphinx-rst-rtd-sample-project/
  python3 -m pip install --user virtualenv
  python3 -m venv venv
  source venv/bin/activate

..code-block:: bash
  mkdir docs
  cd docs
  pip install sphinx

..code-block:: bash
  pip install sphinx-rtd-theme

..code-block:: bash
  pip install sphinx-copybutton

..code-block:: bash
  make html
