
# clustergrammer2

[![Build Status](https://travis-ci.org/ismms-himc/clustergrammer2.svg?branch=master)](https://travis-ci.org/ismms-himc/clustergrammer2)
[![codecov](https://codecov.io/gh/ismms-himc/clustergrammer2/branch/master/graph/badge.svg)](https://codecov.io/gh/ismms-himc/clustergrammer2)

An interactive WebGL heatmap Jupyter widget built using the widget-ts-cookiecutter library.

## Installation

A typical installation requires the following commands to be run:

```bash
pip install clustergrammer2
jupyter nbextension enable --py [--sys-prefix|--user|--system] clustergrammer2
```

Or, if you use jupyterlab:

```bash
pip install clustergrammer2
jupyter labextension install @jupyter-widgets/jupyterlab-manager
```

## Local Development and Relesaing new Versions

#### Webpack

During development run `npm run watch` for real time updates.

Run the following commands to build the JavaScript bundle:

```
$ npm run build
$ npm run build:nbextension
$ npm run build:labextension
```

Publish to npm using
```
$ npm publish
```

These instructions are based on the release instructions from the [jupyter-widgets/widget-ts-cookiecutterREADME](https://github.com/jupyter-widgets/widget-ts-cookiecutter).

## Bundling the Python Package

Next, bundle the python package using

```
$ python setup.py sdist bdist_wheel
```

Then, upload the PYPI:

```
$ twine upload dist/*
```

### Embedding widget
jupyter nbconvert --to html notebook.ipynb