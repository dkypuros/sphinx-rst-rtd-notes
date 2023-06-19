Special section for using GitHub CodeSpaces

```bash

python3 --version
pip --version

cd sphinx-rst-rtd-sample-project/
python3 -m pip install --user virtualenv
python3 -m venv venv
source venv/bin/activate

mkdir docs
cd docs
pip install sphinx

pip install sphinx-rtd-theme

pip install sphinx-copybutton

make html

```
