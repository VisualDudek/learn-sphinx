# learn-sphinx
My Comprehensice Guide to Python Documentation Generation

## Goals

- **Quick Setup**: Guide to quickly setting up a Sphinx documentation project.
- **Using Extensions**: Instructions on how to enhance your documentation with various Sphinx extensions.
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


## Branch
- `dev-init` - init setup for Sphinx