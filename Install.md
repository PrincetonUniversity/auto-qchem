# non-python, install openbabel binary package (we will install python bindings to that package later)
https://github.com/openbabel/openbabel/releases/download/openbabel-2-4-1/OpenBabel-2.4.1.exe

# install latest miniconda

# open miniconda prompt

# create a conda environment
conda create --name autoqchem python=3.7

# activate the environment
conda activate autoqchem

# install mainstream python packages using conda
conda install jupyter pandas scipy matplotlib pymongo pyyaml fabric xlrd appdirs

# Chem packages

# install openbabel (for OSX/Linux this installs the full package, for Windows only the bindings
# to the openbabel Windows installation)
conda install -c conda-forge openbabel=2.4.1



# install imolecule (package to display 3D molecules within jupyter notebooks)
pip install imolecule==0.1.13

# pull autoqchem from github
git clone https://github.com/PrincetonUniversity/auto-qchem.git some_directory

# with your conda environment active and in autoqchem root directory install the package executing
python setup.py install
