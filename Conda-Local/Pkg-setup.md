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

See the ipykernel installation instructions in Setup.md

## Install JupyterLab via conda-forge

Activate your target Conda environment (conda activate <env>), then install JupyterLab from conda-forge:

```sh
conda install -c conda-forge jupyterlab -y
```

## Start JupyterLab Server

Ensure the target environment is active, then launch:

```sh
jupyter lab --no-browser --allow-root --ip 0.0.0.0
```

Notes:
- Default port is 8888; override with --port <PORT>.
- Open the URL (with token) printed in the terminal.
- If accessing remotely, forward the chosen port before opening the URL.
- Enter token Shown in terminAl

```
    To access the server, open this file in a browser:
        file:///home/codespace/.local/share/jupyter/runtime/jpserver-33253-open.html
    Or copy and paste one of these URLs:
        http://codespaces-3f8e71:8888/lab?token=7d94ce6e5cfddd4f520a2295571f6940640735901ba75785 <------ from here
        http://127.0.0.1:8888/lab?token=7d94ce6e5cfddd4f520a2295571f6940640735901ba75785  <------ or here
```

### You're now in JupyterLab & view everything from your current IDE/CODESPACE to JupyterLab

## Install Git Extension for JupyterLab

To enable Git integration within JupyterLab, install the jupyterlab-git extension:

```sh
conda install -c conda-forge jupyterlab-git -y
```

This extension provides a Git GUI directly in JupyterLab for version control operations.

## Stop and Restart JupyterLab Server

If you don't see your newly installed extensions in JupyterLab, you need to stop and restart the server:

### Stop the Server

In the terminal where JupyterLab is running, press `Ctrl+C` twice to stop the server.

### Restart the Server

After stopping, restart JupyterLab with the same command:

```sh
jupyter lab --no-browser --allow-root --ip 0.0.0.0
```

The extensions should now be visible in JupyterLab after the restart.