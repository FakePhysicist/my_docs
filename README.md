# My Docs

[![Jupyter Book Badge](https://jupyterbook.org/badge.svg)](https://github.com/FakePhysicist/my_docs)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue.svg)](https://creativecommons.org/licenses/by-nc/4.0/deed.zh)

## Install jupyter-book

```bash
conda install -c conda-forge jupyter-book
```
or use the provided `environment.yml` file to create a new environment.

```bash
conda env create -f environment.yml
```

## Build the book

since we have a `Makefile` in the root directory, we can simply run

```bash
make html
```

if you want to build the book in a different directory, you can use

```bash
jupyter-book build . --path-output <output_dir>
``` 

## Publish the book online with GitHub Pages

There should be a collection of HTML files in your book’s _build/html folder after you build the book. You can host these files on GitHub Pages to make your book available online.

1. install `ghp-import`

    ```bash
    pip install ghp-import
    ```

2. Make sure your book is built in the 'main' branch and use 'gh-pages' branch to host the book. Choose root directory `/` for the book.

3. From the `main` branch, run

    ```bash
    ghp-import -n -p -f _build/html
    ```
