# python-project-template
A python project template for educational purposes

## Quickstart
1. Create a python virtual environment:  
`python -m venv .venv`
2. Activate your environment:  
`source .venv/bin/activate`
3. If you want install the development requirements:  
`pip install -r requirements.dev.txt`
4. Install pre-commit to use pre-commit hooks:
`pre-commit install`
5. Install the package in development mode:  
`pip install -e .`

## Python venv
**venv** stands for virtual environment and is part of the python standard library (i.e. you don't have to install it).
Python virtual environments' role is to create an isolated python environment for each project so that there are no dependency issues etc. from conflicting project requirements (e.g. Project A need pandas 1.0 and Project B needs pandas 1.1).  

The command `python -m venv .venv` creates a directory call .venv.  
You can activate the virtual environment with `source .venv/bin/activate`. 

To enable the new venv in jupyter notebooks follow the instructions here:  
https://janakiev.com/blog/jupyter-virtual-envs/

link to the venv documentation:  
https://docs.python.org/3/library/venv.html

Alternatives to venv are conda environments but there are some big differences between the 2: 
https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html

## requirements.txt
Requirements files specify the dependencies of the project for other packages.  
How the requirements are distributed across directories and files varries.  
For this project we have 3 files where the requirements are stored: 
* [requirements.dev.txt](requirements.dev.txt) has the dependencies anything that is necessary for the developer but not the user of the package (e.g. testing & linting)
* [docs/requirements.txt](docs/requirements.txt) has the dependencies for building the documentation.
* [setup.py](setup.py) has the **examplepackage** dependencies as part of the `install_requires` parameter of the `setup` function. More info in the dedicated section below.  

The command `pip installs -r requirements.txt` install requirements from the specified file.

Alternatives to using requirements.txt files are conda enviroment yaml files (if you choose to use a conda env that is): 
https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html

## flake8
Quotting the the [flake8 documentation](https://flake8.pycqa.org/en/latest/manpage.html) directly:  
*flake8 is a command-line utility for enforcing style consistency across Python projects. By default it includes lint checks provided by the PyFlakes project, PEP-0008 inspired style checks provided by the PyCodeStyle project, and McCabe complexity checking provided by the McCabe project. It will also run third-party extensions if they are found and installed.*

In summary, flake8 checks if the code is uggly according to [PEP8](https://www.python.org/dev/peps/pep-0008/).
flake8 is part of the requirements.dev.txt file and can be installed with pip.
To run a flake8 check you simply execute the command: 
`flake8 examplepackage` *or any other dir that contains python files* 

You can configure flake8 by adding a section for flake8 in the setup.cfg[setup.cfg] file. For example you can choose to instruct flake8 to ignore certain errors or change the default line length.

## black
*[insert description]*

## pytest
*[insert description]*

## setup.py
*[insert description]*

## setup.cfg
*[insert description]*

## Installing a package in Development mode
*[insert description]*

## .gitignore
*[insert description]*

## Pre-commit hooks
*[insert description]*

## Github Actions
*[insert description]*

## Licences
*[insert description]*

## TO-DOs:
- [ ] Descriptions for each component
- [X] Add documentation using sphynx
- [ ] Add branch protection rules
- [ ] Add a Makefile for ease of use
