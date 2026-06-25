# Project Setup

## Prerequisites

* Python installed
* `pyenv` installed
* `pyenv-virtualenv` plugin installed
* Git installed

---

## Create and Activate Virtual Environment

Create a new virtual environment named `mkdocs`:

```bash
pyenv virtualenv mkdocs
```

Activate the virtual environment:

```bash
pyenv activate mkdocs
```

Verify that the environment is active:

```bash
python --version
which python
```

---

## Install Dependencies

Install all required Python packages from `requirements.txt`:

```bash
pip install -r requirements.txt
```

If `pip` is not installed or needs to be upgraded:

```bash
python -m ensurepip --upgrade
pip install --upgrade pip
```

---

## Run Locally

Start the local MkDocs development server:

```bash
mkdocs serve
```

The documentation will be available at:

```text
http://127.0.0.1:8000
```

MkDocs automatically reloads when files are modified.

---

## Deploy to GitHub Pages

Deploy the documentation site to GitHub Pages:

```bash
mkdocs gh-deploy
```

This command:

1. Builds the static site.
2. Pushes the generated files to the `gh-pages` branch.
3. Publishes the site through GitHub Pages.

After deployment, site will be available at:

```text
https://kalpavriksha-edu.github.io/portal/
```

---

## Useful Commands

### Generate/Update requirements.txt

```bash
pip freeze > requirements.txt
```

### Build Static Site

```bash
mkdocs build
```

The generated site will be created in the `site/` directory.

### Check MkDocs Configuration

```bash
mkdocs build --strict
```

This validates the documentation and configuration for errors.
