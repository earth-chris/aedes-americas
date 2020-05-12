# aedes-americas

Continental-scale species distribution modeling for Aedes aegypti and Ae. albopictus, the mosquito vectors of dengue, chikungunya and Zika.

## Introduction

Link to paper.

This repository contains the code and notebooks used to generate and reproduce the results from this paper.

## Setup

This workflow is designed to install and run via `conda`. You can find `conda` install instructions [here][home-conda]. 


```bash
# download the repository
git clone https://github.com/earth-chris/aedes-americas.git
cd aedes-americas

# install the conda package
conda env update
conda activate aedes
```

The one non-traditional dependency here is the `ccb` package, a python wrapper for running `maxent` species distribution models. You can read about the `ccb` package [on GitHub][home-ccb]. Download and install this package from within the `aedes-america` directory.

```
# download and install the ccb package
git clone https://github.com/stanford-ccb/ccb.git
cd ccb
pip install -r requirements.txt
python setup.py install

# the following is optional to use the ccb default ipython config
conda env config vars set IPYTHONDIR=$PWD/ipython
```



## Running the notebooks

```bash
conda activate aedes
jupyter notebook
```

From this directory, notebooks are organized into the `data-processing`, `modeling` and `plots-and-analysis` directories. Load and explore these notebooks to understand their functions.


[home-ccb]: https://github.com/stanford-ccb/ccb
[home-conda]: https://docs.conda.io/