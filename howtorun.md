# How to view/ Run these Notebooks

These tutorials are written as [Jupyter Notebooks](https://jupyter-notebook.readthedocs.io/en/stable/), we highly recommend they are run on the tested university GPU machines which have the required hardware and software. Below are instruction on how to run the notebooks on the university machines both locally and remotely. It is possible to run these notebooks on google colab and personal laptops and we provide instructions for those non preferred methods, however anyone outside of the university of leeds wishing to run these notebooks would need to use these. 

## In class on University of leeds machines

1. log in to GPU work stations using university of leeds credentials
2. load python environment `module add condaenv/unet-2024-10-07`
3. Download Git repo *should we store this centrally so students don't have to do git logins etc or via wget*
4. launch notebook server: `jupyter-notebook`

## Using university machines remotely

1. ssh to the university machines either via remote-access machine, on the wired network or via vpn
   
    `ssh -o PreferredAuthentications=password -o PubkeyAuthentication=no  -X uol-pc-055688`
2. Load python environment `module add condaenv/unet-2024-10-07`
3. Fist time only, all subsequent times proceed to step 4

    generate a default config file and set a password
   
    `jupyter notebook --generate-config`
   
    `jupyter notebook password`
   
    edit config file
   
    `gedit .jupyter/jupyter_notebook_config.py`
   
    make the following edits:

```
c.ServerApp.allow_origin = '*'
c.ServerApp.allow_remote_access = True
c.ServerApp.local_hostnames = ['0.0.0.0']
# c.ServerApp.open_browser = False #optional
c.ServerApp.port = 55555 # chose a different number!
```

4. git clone the repo you require
5. Run `jupyter-notebook`
   
    you should see a message that looks something like this:

   Take Note of port number e.g. 5566
   
6. Now on your machine (you must be on vpn or wired university network, or have configured you ssh to work without)
  * generic    `ssh -N -f -L localhost:<localportno>:localhost:<remoteportno> user@host`
  * following this example:
     `ssh -N -f -L localhost:5000:localhost:5566 user@uol-pc-055688`
7. Access from your local browser `http://localhost:5000/` enter your password

**Tip** only one person can use each port number on each machine replace 5566 with another random 4 digit number 

## Google CoLab

If the notebook works with Google CoLab then there will be an open with google colab button and some additional instructions in grey boxes.

## Using your own machine

All notebook are accompanied by a .yml fil which can be used to install a python environment.

It is recommended you use [anaconda](https://docs.anaconda.com/anaconda/install/) or [mamba](https://mamba.readthedocs.io/en/latest/installation/mamba-installation.html) to manage the python packages required. Sore Machine learning libraries are large and if you only wish to run one notebook consider installing the environment provided for that specific notebook. Otherwise, you can install all required packages running the following commands.  

```bash
conda env create -f <env-file>.yml
conda activate <env-name>
# save yourself some space with one extra command
conda clean -a
jupyter-notebook # launches the notebook server
```

For a quicker installation you may wish to use mamba for more information Berkley university has written a nice guide on this at [https://statistics.berkeley.edu/computing/conda](https://statistics.berkeley.edu/computing/conda)
