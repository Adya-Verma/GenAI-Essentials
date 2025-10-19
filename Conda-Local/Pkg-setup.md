# To Install Packages in Your Environment

This section provides instructions for installing packages in your Conda environment. Use the following commands to add packages to your active environment:

### Basic Package Installation

```sh
conda activate
conda install -c conda-forge pandas
```

### Note on Package Sources

**Tip:** You can use `conda-forge` instead of `pip install` for most packages. Conda-forge is a community-led collection of recipes, build infrastructure, and distributions for the conda package manager.

For more information, visit the [conda-forge website](https://conda-forge.org/).

## Install from requirements.txt

Use a requirements.txt to install Python packages with pip into your active Conda environment. List one package per line and optionally pin versions (for example: requests==2.32.*, scikit-learn>=1.5,<2, uvicorn[standard]). Activate the environment first (conda activate <env>). Prefer conda-forge when available; use pip for the rest.
```sh
pip install -r requirements.txt 
```

