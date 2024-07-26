# learn-sphinx
My Comprehensice Guide to Python Documentation Generation

## Goals

- **Quick Setup**: Guide to quickly setting up a Sphinx documentation project.
- **Using Extensions**: Instructions on how to enhance your documentation with various Sphinx built-in extensions, e.g. `autodoc` and `napoleon`.
- **GitHub Actions to Generate Docs from Docstrings**: Automate the generation of documentation from docstrings using GitHub Actions.
- **Autodocs for Unittests**: Integrate unit tests documentation automatically into your Sphinx-generated docs.


### Quick Setup
- Install Sphinx package
```bash
pip install sphinx
```
- Create `docs/` dir and run insde `sphinx-quickstart`, this will create docs structure. 
- Key two files: `index.rst` and `conf.py`.

Use `Makefile` to build the docs
```bash
make html
```

- Populate `index.rst` and create other documentation source files.

### Using `autodoc` and `napoleon` Extensions
- add extenstions (no install needed, built-in) into `conf.py`:
```python
# conf.py
extensions = [
    'sphinx.ext.autodoc',
    'sphinx.ext.napoleon',
]
```
- make sure the code can be imported, recomended way is to follow Python-SOP and install code in editable mode (you will need `setup.py` or better)
```bash
pip install -e .
```
- add `automodule` Directive into `*.rst` doc-file, e.g.:
```md
my_project/
├── README.md
├── requirements.txt
├── setup.py
├── src/
│   ├── neptun/
│   │   ├── __init__.py
│   │   └── main.py
├── tests/
│   ├── __init__.py
│   └── test_main.py
├── .devcontainer/
│   └── devcontainer.json
└── docs/
    └── index.md
```
```rst
.. automodule:: neptun.main
    :members:
```
- build docs
```
make html
```

# Dev Notes

## Branch
- `dev-init` - init setup for Sphinx
- `dev-ext` - use built-in extentions, `autodoc` and `napoleon`