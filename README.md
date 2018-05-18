# dl-workshop

Intro to deep learning workshop.

## Install before the workshop

You might be working on other Python projects at the moment that use some of the libraries from the workshop - but at different versions. To avoid breaking your current setup - and to simplify the installation process - we will use **Conda environments**.

The idea is to create a `dl-workshop` environment for the workshop that you can activate when you work on it and then deactivate to restore your original configuration.

### Step 1 - Install Conda

We will use `Conda` to install the Python libraries for the workshop. You can get it by installing [Anaconda (Python 3.6 version)][anaconda-download].

[anaconda-download]:https://www.anaconda.com/download/

Verify that it's installed by running the following command in a terminal (on macOS or Linux) or the "Anaconda Prompt" on Windows. The command should return its version number.

```bash
conda -V
```

Make sure that you have a recent version (see [changelog][conda-changelog]). To update `Conda`, navigate to its folder (usually in your home directory) and run

```bash
conda update conda
```

[conda-changelog]:https://github.com/conda/conda/blob/master/CHANGELOG.md

### Step 2 - Install the environment

If you correctly installed `Conda`, you should be able to list the current environments by running this command in a terminal (or the Anaconda Prompt for Windows users).

```bash
conda env list
```

Let's create a `dl-workshop` entry for the workshop. Start by downloading this GitHub repository ("download" button from above) and extract it on your computer. The folder contains `.yml` configuration files that list the libraries needed for the workshop with their version number. Use the file that matches your setup - Windows, macOS or Linux.

To create the environment, open your terminal and navigate to the folder with the `.yml` files. You can then install the environment by typing `conda create -f ..` with the appropriate file.

```bash
# For Windows users
conda create -f environment-windows.yml

# On macOS
conda create -f environment-macos.yml

# .. Linux
conda create -f environment-linux.yml
```

This operation might take some time. Verify that the environment is installed with `conda env list`.

### Step 3 - Activate and deactivate it

You can **activate** the environment with

```bash
# On Windows
activate dl-workshop

# On macOS and Linux
source activate dl-workshop
```

*__Troubleshooting__: If this doesn't work for you, then it's likely that Conda doesn't find the environment. Is it installed?*

Now, everything that you do from this terminal uses the libraries from the `dl-workshop` environment. To launch the Jupyter interface, type

```
# Open the Jupyter dashboard
jupyter notebook

# Or the new "Jupyter lab" one
jupyter lab

# You can then quit the interface with Ctrl+C
```

Similarly, you can **deactivate** the environment with

```bash
# On Windows
deactivate

# On macOS and Linux
source deactivate
```
