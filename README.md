# Virtual Screening Case Study
## Bioinformatics approaches in adhesion GPCR research
![logo](https://user-images.githubusercontent.com/109313212/188150093-a309b31c-c12d-4d00-be4c-ad51d877599f.png)


This is a material for Day 1 where we will get our hands dirty with some more advanced usage of open source toolkits for docking-based virtual screening (VS).

This part of the training session is organized as a case study where practical application of virtual screening in aGPCR research will be introduced to the participants.

During this session, the participants will learn:
- What is the VS and why it's important in modern research;
- How to perform VS using open source software;
- How to critically analyze results of VS and molecular docking;
- How to apply these protocols on any protein target of interest?

We will work under Anaconda platform in order to keep this tutorial scalable and operating system independent as much as possible (so everyone could easily apply this code to their own research at home institutions).
In order for everything to be flawless, participants should install all packages before training school following installation instructions bellow.
## Google Colab notebook
As additional learning resource, we provide Google Colab notebook.
If something goes wrong with installation, just switch to the Colab.
https://colab.research.google.com/drive/18OzRUdbWoG3lSc3ZtItzBFQ_A-jXZpzp?usp=sharing

## Installation instructions
1. Install the Anaconda (https://www.anaconda.com/products/distribution) using the instructions for your operating system (https://docs.anaconda.com/anaconda/install/). Installation should be straightforward. Before proceeding with next step, Linux and macOS users should not forget to restart a shell (terminal) after installation. 
2. Open the terminal (for Windows users open Anaconda Powershell Prompt) and type following commands (line by line):
- `conda create -n oddt python=3.9`
- `conda activate oddt`  - this is used to activate anaconda enviroment under we will be working for the rest of the session
- `conda install -c conda-forge rdkit openbabel`
- `conda install -c oddt oddt`
- `conda install -c anaconda ipykernel`
- `python -m ipykernel install --user --name=oddt`
- `conda install py3dmol -c conda-forge`
- `conda install -c conda-forge prolif`
3. Download AutodockVina.py from this repository. Then, replace (copy/paste) AutodockVina.py from created oddt anaconda environment with downloaded file (detailed instructions below).
- Windows users: Replace AutodockVina.py from the location: C:\Users\Korisnik\anaconda3\envs\oddt\Lib\site-packages\oddt\docking (C:\Users\Korisnik should be replaced with name of your machine). If there is no such file at this location, use File Explorer to search.
- Linux users: Replace AutodockVina.py from the location: /home/user/anaconda3/envs/oddt/lib/python3.9/site-packages/oddt/docking/ (/home/user/ should be replaced with name of your machine). In case you cannot locate, type `find /home/user/anaconda3/envs/ -iname AutodockVina.py` in your terminal. This command will locate the file.
- macOS users should follow instructions for Linux users, although I am not sure that location would be the same. Anyhow, everything should be under the /anaconda3 folder so in case you cannot locate manually (using search bar), type `find /path/to/anaconda3/folder/ -iname AutodockVina.py` in your terminal.
- Special case are those who do not have admin privileges. In this case, location is hidden and could be accessed by terminal at ~/.conda/envs/oddt/lib/python3.9/site-packages/oddt/docking/AutodockVina.py (Linux users). Use the cp command to replace the file. If you cannot proceed, please contact me.
4. To check everything, type `jupyter notebook` in terminal with active oddt environment (`conda activate oddt` above). Jupyter notebook should open in your browser. 
5. Install Marvin suite (https://chemaxon.com/products/marvin) (it requires registration, but it is free for academics and offers 2 months renewable trial licenses for non-academics). This is not obligatory step, but useful.
6. Download Gypsum-DL from https://durrantlab.pitt.edu/gypsum-dl/

