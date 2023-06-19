Special section for using GitHub CodeSpaces

```bash
python3 --version
pip --version
```

```bash
cd sphinx-rst-rtd-sample-project/
python3 -m pip install --user virtualenv
python3 -m venv venv
source venv/bin/activate
```

```bash
mkdir docs
cd docs
pip install sphinx
```

```bash
pip install sphinx-rtd-theme
```

```bash
pip install sphinx-copybutton
```

```bash
make html
```

```bash
pip install sphinx-autobuild
```

```bash
sphinx-autobuild --host 0.0.0.0 --port 8000 docs/source docs/build/html
```

