# Example Python Package

This is a working Python Package that can be installed either locally
or via pip from the pypi repository. 

The package contains classes for a normal and a binary probabiity distribution.
This package is currently uploaded to [PyPi](https://pypi.org/project/example-probability/) and can be pip installed with the command `pip install example_probability'. 

This document explains how to pip install the package as well as how to upload the package to the PyPi repository.

# Getting Started

## Files

Explanation of files in the package
* setup.py - file necessary for pip installing
* dsnd_probability - folder with the files that make up the Python package

## Prerequisites

You must have python3 installed and the matplotlib package

## Installing

Here are instructions for installing the package locally

1. Clone or download the repository
2. From the command line, cd into the python-package directory
3. Create a virtual environment with the command `python3 -m venv tutorial_venv` where tutorial_venv is the name of your virtual environment. This name can be whatever you choose.
4. Activate the virtual environment with `source tutorial_venv/bin/activate`
5. Enter the command `pip install .`. This will install the python_example_package into your virtual environment

You should now be able to use the package in a Python program using an import statement like `import dsnd_probability`.

# Deployment

To deploy the package to PyPi, you'll first need to come up with a new name for the package. The folder containing the package files should be changed as well as the package names in the setup.py. This is because PyPi only allows one package to have a specific name.

To upload a package to the PyPi repository, enter the following commands in the terminal:

```
python3 -m pip install --user --upgrade setuptools wheel
```

Cd into the package directory with the setup.py file and run:
```
python3 setup.py sdist bdist_wheel
```

Finally run the following commands:
```
python3 -m pip install --user --upgrade twine
twine upload dist/*
```

You'll be asked for your PyPi username and password. If you do not have 
an account yet, then first sign up for one at the [PyPi](https://pypi.org) website.

You can now pip install the package using the command `pip install example_probability`.