# EuroSciPy 2019 - scikit-learn tutorial

All notebook material: https://github.com/lesteve/euroscipy-2019-scikit-learn-tutorial/

Some intro slides: http://ogrisel.github.io/decks/2017_intro_sklearn

## Follow the tutorial online

- Launch an online notebook environment using [![Binder](https://mybinder.org/badge_logo.svg)](
               https://mybinder.org/v2/gh/lesteve/euroscipy-2019-scikit-learn-tutorial/master?urlpath=lab)

- Browse the static content online (pre-rendered outputs) using [nbviewer](
  https://nbviewer.jupyter.org/github/lesteve/euroscipy-2019-scikit-learn-tutorial/tree/master/rendered_notebooks/)

You need an internet connection but you will not have to install any package
locally.


## Running the tutorial locally

### Dependencies

The tutorials will require the following packages:

* python>=3.6
* jupyter
* scikit-learn
* pandas
* pandas-profiling
* matplotlib
* seaborn

### Local install

We provide both `requirements.txt` and `environment.yml` to install packages.

You can install the packages using `pip`:

```
$ pip install -r requirements.txt
```

You can create an `sklearn-tutorial` conda environment executing:

```
$ conda env create -f environment.yml
```

and later activate the environment:

```
$ conda activate sklearn-tutorial
```

You might also only update your current environment using:

```
$ conda env update --prefix ./env --file environment.yml  --prune
```

## Contributing

This repo uses: [Jupytext doc](https://jupytext.readthedocs.io/)

To synchronize the notebooks and the Python scripts (based on filestamps, only
input cells content is modified in the notebooks):

```
$ jupytext --sync notebooks/*.ipynb
```

or simply use:

```
$ make sync
```

If you create a new notebook, you need to set-up the text files it is going to
be paired with:

```
$ jupytext --set-formats notebooks//ipynb,python_scripts//py:percent notebooks/*.ipynb
```

or simply use:

```
$ make format
```

To render all the notebooks (from time to time, slow to run):

```
$ make render
```


## Direct binder links to GKE and OVH to trigger and cache builds

- [GKE Binder](https://gke.mybinder.org/v2/gh/lesteve/euroscipy-2019-scikit-learn-tutorial/master?urlpath=lab)

- [OVH Binder](https://ovh.mybinder.org/v2/gh/lesteve/euroscipy-2019-scikit-learn-tutorial/master?urlpath=lab)
