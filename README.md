
# SOSTAT2021: 2nd IAA-CSIC Severo Ochoa School on Statistics, Data Mining, and Machine Learning

## A Severo Ochoa School of the Instituto de Astrofísica de Andalucía (CSIC)

![SOMACHINE](tutorials/iaa-so-csic.png)

School webpage: https://www.granadacongresos.com/sostat2021

- [Workshop Tutorials](#workshop-tutorials)
- [Execution of the tutorials](#execution-of-the-tutorials)
- [Two alternative ways to execute the tutorials](#two-alternative-ways-to-execute-the-tutorials)
  * [1. In your local machine](#1-in-your-local-machine)
    + [Install conda](#install-conda)
    + [Get the contents of the school](#get-the-contents-of-the-school)
  * [2. Using the myBinder cloud](#2-using-the-mybinder-cloud)
- [Credits and acknowledgements](#credits-and-acknowledgements)

# Workshop Tutorials

- Gwendolyn Eadie
    - [Sampling from distributions with R](tutorials/gwen_probability/sampling_from_distributions_with_R.ipynb)

- Željko Ivezić
    - [ZIlecture1: Gentle Introduction to Big Data in Astronomy and Basics](tutorials/zeljko/ZIlecture1.ipynb)
    - [ZIlecture2: Introduction to ML; density estimation and regression](tutorials/zeljko/ZIlecture2.ipynb)
- Abigail Stevens
    - [boot_jack_workbook](tutorials/abigail_bootjack/boot_jack_workbook.ipynb) ([solutions](tutorials/abigail_bootjack/boot_jack_solutions.ipynb))
    - [time_series_workbook](tutorials/abigail_timeseries/time_series_workbook.ipynb) ([solutions](tutorials/abigail_timeseries/time_series_solutions.ipynb))
    
- Daniela Huppenkothen
    - [Practical Machine Learning with SDSS Data](tutorials/daniela_machine_learning/SOSTAT2021_ML_Tutorial.ipynb) ([solutions](tutorials/daniela_machine_learning/SOSTAT2021_ML_Tutorial_SOLUTIONS.ipynb))
    - [A Tutorial on Neural Networks](tutorials/daniela_neural_networks/SOSTAT2021_NN_Tutorial_SOLUTIONS.ipynb)

# Execution of the tutorials

The [IAA-CSIC Severo Ochoa Center](http://so.iaa.csic.es/) provides a JupyterHub server available during the duration of the school here:

[https://spsrc-jupyter.iaa.csic.es/sostat2021/](https://spsrc-jupyter.iaa.csic.es/sostat2021/)

Login with the credentials provided to you. These instances will have persistent storage throughout the duration of the school. **All virtual machines and their contents will be removed by the 2021-12-12.**. In case of any problem, please fill an [issue here](https://github.com/spsrc/sostat2021/issues) or ask in the #help Slack channel.


# Two alternative ways to execute the tutorials


## 1. In your local machine

### Install conda

We recommend using `conda` to manage the dependencies. Miniconda is a light-weight version of Anaconda. First we show how to install Miniconda if you don't have it already. More details [here](https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html)

You can skip this step if you already have conda available in your path.

Miniconda for Linux:
```bash
curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash ./Miniconda3-latest-Linux-x86_64.sh
rm ./Miniconda3-latest-Linux-x86_64.sh
```

Miniconda for macOS:
```bash
curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
bash Miniconda3-latest-MacOSX-x86_64.sh
rm Miniconda3-latest-MacOSX-x86_64.sh
```

That is all, `conda` should be available in your path. Note that the installation will suggest you to modify your bashrc so conda is always available, which is a good idea in general. Alternatively, if you want the Miniconda installation to be encapsulated in your working directory without affecting the rest of your system you can install it with the following option. The first command only needs to be done once, and the second one needs to be done everytime you open a new terminal. 

```bash
cd /your/working/directory/
bash ./Miniconda3-latest-Linux-x86_64.sh -b -p my_conda_env
source my_conda_env/etc/profile.d/conda.sh
```

### Get the contents of the school

Download this repository and create the conda environment with the dependencies
```bash
git clone https://github.com/spsrc/sostat2021.git
cd sostat2021
conda env create -f environment.yml
conda activate sostat2021
```

If you want to use Jupyer Lab, start it and navigate to `tutorials/index.html` with:
```bash
jupyter lab
```

## 2. Using the myBinder cloud

At any moment, also after the school, you can still run the tutorials in [myBinder.org](https://mybinder.org) following this link: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/spsrc/sostat2021/HEAD?urlpath=lab/tree/tutorials/index.ipynb)

[myBinder.org](https://mybinder.org) is a free and open organization providing free cloud resources. Therefore, the resources may be limited and the changes you make in the notebooks or the system are not persistent. Please, always keep a local copy of any file you want to keep, because Binder will automatically eliminate the virtual machine assigned to you after some time of inactivity.


# Credits and acknowledgements

This repository and the Jupyter Hub service for the tutorials are provided by the SKA Regional Centre Prototype (SPSRC), which is funded by the State Agency for Research of the Spanish MCIU through the "Center of Excellence Severo Ochoa" award to the Instituto de Astrofísica de Andalucía (SEV-2017-0709), the European Regional Development Funds (EQC2019-005707-P), the Junta de Andalucía (SOMM17_5208_IAA), and the project RTI2018-096228-B-C31(MCIU/AEI/FEDER,UE) and the grants PTA2018-015980-I(MCIU,CSIC) and 54A Scientific Research and Innovation Program (Regional Council of Economy, Knowledge, Business and Universities, Regional Government of Andalusia and the European Regional Development Funds 2014-2020, program D1113102E3).
