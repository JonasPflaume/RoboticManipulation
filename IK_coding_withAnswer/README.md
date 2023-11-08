1. Install miniconda or anaconda

https://docs.conda.io/projects/miniconda/en/latest/

You can deactivate the conda by commenting the corresponding lines in your ~/.bashrc.

2. Install the necessary packages

conda env create -f environment.yml (You will need to modify the prefix in environment.yml)
conda activate ik_env
python -m ipykernel install --user --name=ik_env

if conda solving environment last forever, 
you could install the following solver to speed up

conda update -n base conda
conda install -n base conda-libmamba-solver
conda config --set solver libmamba

3. run the notebook 

jupyter notebook

* Don't forget to switch kernel inside the notebook to ik_env!
* If you used gepetto-gui, you would need to adjust the perspective inside the GUI to show the whole robot properly.
