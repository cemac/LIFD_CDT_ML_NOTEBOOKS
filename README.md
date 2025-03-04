<div align="center">
<img src="https://github.com/cemac/LIFD_ENV_ML_NOTEBOOKS/blob/main/images/LIFDlogo.png"></a>
<a href="https://www.cemac.leeds.ac.uk/">
  <img src="https://github.com/cemac/cemac_generic/blob/master/Images/cemac.png"></a>
  <br>
</div>

# Leeds Institute for Fluid Dynamics Machine Learning CDT Notebooks #
## Jupyter Notebooks ##

 [![GitHub release](https://img.shields.io/github/release/cemac/LIFD_CDT_ML_NOTEBOOKS.svg)](https://github.com/cemac/LIFD_CDT_ML_NOTEBOOKS/releases) [![GitHub top language](https://img.shields.io/github/languages/top/cemac/LIFD_CDT_ML_NOTEBOOKS.svg)](https://github.com/cemac/LIFD_CDT_ML_NOTEBOOKS) [![GitHub issues](https://img.shields.io/github/issues/cemac/LIFD_CDT_ML_NOTEBOOKS.svg)](https://github.com/cemac/LIFD_CDT_ML_NOTEBOOKS/issues) [![GitHub last commit](https://img.shields.io/github/last-commit/cemac/LIFD_CDT_ML_NOTEBOOKS.svg)](https://github.com/cemac/LIFD_CDT_ML_NOTEBOOKS/commits/master) [![GitHub All Releases](https://img.shields.io/github/downloads/cemac/LIFD_CDT_ML_NOTEBOOKS/total.svg)](https://github.com/cemac/LIFD_CDT_ML_NOTEBOOKS/releases) ![GitHub](https://img.shields.io/github/license/cemac/LIFD_CDT_ML_NOTEBOOKS.svg)


[![Bluesky](https://img.shields.io/badge/Bluesky-0285FF?logo=bluesky&logoColor=fff)](https://bsky.app/profile/lifd.bsky.social)


The Leeds Institute for Fluid Dynamics (LIFD) has teamed up with the Centre for Environmental Modelling and Computation (CEMAC) to create Jupyter notebook teaching materials for the LIFD CDT.

1. [Physics Informed Neural Networks](https://github.com/cemac/https://github.com/cemac/LIFD_Torch_PINNS)
2. [Image Segmentation](https://github.com/cemac/LIFD_ImageSegmentation)
3. [Autoencoders](https://github.com/cemac/LIFD_TorchAutoEncoders)
4. [Design Optimisation with Metamodels](https://github.com/cemac/LIFD_DesignOptimisation)
5. [Modal Decomposition](https://github.com/cemac/LIFD_ModalDecomposition)


**PLEASE NOTE YOU MUST CLONE RECURSIVELY (SEE BELOW)**

These notebooks are designed to run alongside a teaching module, however the notebook for each topic will include links to further reading where necessary. Each notebook will take about two hours to run through and should run out-of-the-box on home installations of Jupyter notebooks, although they have been primarily designed to work on Leeds-based GPU workstations. These notebooks are designed with automatic checking of Python environment files to remain easy to set up into the future.

As this resource grows, in order not to make the repository unwieldy, this repository is made up of submodules that can be cloned individually.

## How do I get started?

Some tutorials are so lightweight you can run them on [binder](https://mybinder.readthedocs.io/en/latest/#what-is-binder). The others we recommend running on your local machine. To get started, either clone this repository (**LARGE SIZE**) or select a tutorial to clone and run each tutorial separately.

### Cloning the whole repository

```bash
git clone --recursive git@github.com:cemac/LIFD_CDT_ML_NOTEBOOKS.git
```

then follow the individual README.md instructions for each notebook.

### Cloning individual tutorials

Instructions for cloning an individual tutorial can be found in the README.md file on that tutorial's GitHub page.


## How to Run

These notebooks can run with the resources provided and the Anaconda environment set up. If you are familiar with Anaconda, Jupyter notebooks and GitHub then simply clone this repository and run it within your Jupyter notebook setup. Otherwise, please read the [how to run](howtorun.md) guide. Individual notebooks have bespoke instructions.


## Requirements

**Python**

It is recommended you use [Anaconda](https://medium.com/pankajmathur/what-is-anaconda-and-why-should-i-bother-about-it-4744915bf3e6) to manage the Python packages required. Some machine-learning libraries are large and if you only wish to run one notebook consider installing the environment provided for that specific notebook. Otherwise, you can install all required packages running the following commands.

```bash
conda env create -f <env-file>.yml
conda activate <env-name>
# save yourself some space with one extra command
conda clean -a
```

**What if I forgot to clone recursively?**

Not to worry. In your cloned folder simply run:

```bash
git submodule init
git submodule update --init --recursive
```

**Hardware**

These notebooks are designed to run on a personal computer. Note that some of the techniques demonstrated are computationally intensive, so there may be options to skip steps within certain notebooks depending on the hardware available, e.g. use pre-trained models.

**Knowledge**

We have assumed some foundational knowledge but links are provided to in-depth information on the fundamentals of each concept.

## Contributions

We hope that this resource can be built upon to provide a wealth of training material for Earth-science machine-learning topics at Leeds.

# Licence information #

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">LIFD_CDT_ML_NOTEBOOKS</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://cemac.leeds.ac.uk/" property="cc:attributionName" rel="cc:attributionURL">cemac</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## Acknowledgements

*Leeds Institute of Fluid Dynamics*, *CEMAC*, *Donald Cummins*, *Helen Burns*, *Peter Jimack*, *Phil Livermore*, *Jonathan Coney*, *Andrew Ross*, *Toni Lassila*, *Calum Skene*, *Arash Rabbani*
