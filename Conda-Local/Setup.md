# Miniconda Setup

## Install Miniconda on Local Environment

Run the following commands to install Miniconda:

```sh
mkdir -p ~/miniconda3
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh -o ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm ~/miniconda3/miniconda.sh
```

## Initialize Conda by running:

```sh
source ~/miniconda3/bin/activate
conda init --all
```

## Create a new env

```sh
conda create --name newenv python=3.10.0 -y
# Replace 'newenv' with any environment name & verşion you prefer 
```

## Activate the env

```sh
conda activate newenv
```

## For info on current env

```sh
conda info
```

## Remove an env

```sh
conda deactivate
conda remove -n hello --all -y 
# Replace 'newenv' with any environment name of your env 

```