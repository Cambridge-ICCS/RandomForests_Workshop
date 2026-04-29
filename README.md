<img src="./images/UCAM_ICCS_Logo.png"  width="600">

# Random Forests

This repository contains documentation, resources, and code for the `Random Forests` session
designed and delivered by Dr. Robert Edwin Rouse of [ICCS](https://github.com/Cambridge-ICCS).  
All materials, including slides and videos, are available such that individuals can cover the
course in their own time.


## Contents

- [Learning Objectives](#learning-objectives)
- [Teaching material](#teaching-material)
- [Preparation and prerequisites](#preparation-and-prerequisites)
- [Installation and setup](#installation-and-setup)
- [License information](#license)
- [Contribution Guidelines and Support](#contribution-guidelines-and-support)


## Learning Objectives

The key learning objective from this workshop could be simply summarised as:
_Provide participants with an intuitive understanding of the theory behind Random Forests and the ability to develop Random Forest and related models_.

However, more specifically we will aim to:

* Provide an understanding of decision trees; 
* Provide an understanding of random forests;
* Cover the strengths and weaknesses of random forests;
* Investigate model explainability and interpetability;
* Explore their practical considersations and applications.

With regards to specific content we cover:

* Using Random Forests for **regression**;
* Using Random Forests for **classification**;
* Visualisation of trained model results;
* Model and feature evaluation using standard metrics.


## Teaching Material

### Slides
The slides for this workshop can be found in the [slides](slides/) directory.  

### Exercises
The exercises for the course can be found in the [exercises](exercises/) directory.  
These take the form of partially complete jupyter notebooks.

### Worked Solutions
Worked solutions for all of the exercises can be found in the [worked solutions](worked-solutions/) directory.  
These are for recapping after the course in case you missed anything, and contain example solutions.


## Preparation and prerequisites

### Prerequisites

To get the most out of the session we assume a basic understanding in a few areas and 
for you to do some preparation in advance.
Expected knowledge is outlined below, along with resources for reading if you are unfamiliar.


### Mathematics and Machine Learning

Basic mathematics knowledge:
- probability theory
- matrix algebra - matrix multiplication and representing data as a matrix
- set theory - relating to permutations
- machine learning - background theory of learning and fitting models to data
- logistic regression

### Python
The course will be taught in python using scikit-learn.
Whilst no prior knowledge of scikit-learn is expected we assume users are familiar with the basics of Python3.
This includes:
- Basic mathematical operations
- Writing and running scripts/programs
- Writing and using functions
- The concept of [object orientation](https://eli5.gg/Object-oriented%20programming)  
  i.e. that an object, e.g. a dataset, can have associated functions/methods associated with it.
- Basic use of the following libraries:
  - [`numpy`](https://numpy.org/) for mathematical and array operations
  - [`matplotlib`](https://matplotlib.org/) for ploting and visualisation
  - [`pandas`](https://pandas.pydata.org/docs/getting_started/index.html) for storing and accessing tabular data
- Familiarity with the [concept of a jupyter notebook](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/index.html)

### git and GitHub
You will be expected to know how to
- clone and/or fork a repository,
- commit, and
- push.

The [workshop from the 2022 ICCS Summer School](https://www.youtube.com/watch?v=ZrwzK4CnJ3Q) 
should provide the necessary knowledge.


### Preparation

In preparation for the course please ensure that your computer contains the following:
- A text editor - e.g. vim/[neovim](https://neovim.io/), [gedit](https://gedit.en.softonic.com/), [vscode](https://code.visualstudio.com/), [sublimetext](https://www.sublimetext.com/) etc. to open and edit code files
- A terminal emulator - e.g. [GNOME Terminal](https://help.gnome.org/users/gnome-terminal/stable/), [wezterm](https://wezfurlong.org/wezterm/index.html), [Windows Terminal (windows only)](https://learn.microsoft.com/en-us/windows/terminal/), [iTerm (mac only)](https://iterm2.com/)
- python virtual environment (see [Installation and setup](#installation-and-setup))

Note for Windows users: _We have linked suitable applications for windows in the above lists.
However, you may wish to refer to [Windows' getting-started with python information](https://learn.microsoft.com/en-us/windows/python/beginners)
for a complete guide to getting set up on a Windows system._

If you require assistance or further information with any of these please reach out to
us before a training session.


## Installation and setup

We have provided intructions below for participating in this workshop via a [local install](#local-install), as it is the easiest way to keep a copy of your work and push back to GitHub.


### Local Install

#### 1. Clone or fork the repository
Navigate to the location you want to install this repository on your system and clone
via https by running:
```
git clone https://github.com/Cambridge-ICCS/RandomForests_SummerSchool25.git
```
This will create a directory `RandomForests_SummerSchool25/` with the contents of this repository.

Please note that if you have a GitHub account and want to preserve any work you do
we suggest you first [fork the repository](https://github.com/Cambridge-ICCS/RandomForests_Workshop/fork) 
and then clone your fork.
This will allow you to push your changes and progress from the workshop back up to your
fork for future reference.

#### 2. Create a virtual environment
Before installing any Python packages it is important to first create a Python virtual environment.
This provides an insulated environment inside which we can install Python packages 
without polluting the operating systems' Python environment.

If you have never done this before don't worry: it is *very* good practice, especially 
when you are working on multiple projects, and easy to do.

```
python3 -m venv RFvenv
```
This will create a directory called `RFvenv` containing software for the virtual environment.
To activate the environment run:
```
source RFvenv/bin/activate
```
You can now work on python from within this isolated environment, installing packages
as you wish without disturbing your base system environment.

When you have finished working on this project run:
```
deactivate
```
to deactivate the venv and return to the system python environment.

You can always boot back into the venv as you left it by running the activate command again.

#### 3. Install dependencies

It is now time to install the dependencies for our code, for example PyTorch.
The project has been packaged with a [`pyproject.toml`](pyproject.toml) so can be installed in one go.
From within the root directory in a active virtual environment run:
```
pip install .
```
This will download the relevant dependencies into the venv as well as setting up the
datasets that we will be using in the course.\
Whilst the workshop should install and run with the latest versions of python libraries,
it has been tested with following versions for major dependencies: pandas 2.3.0, palmerpenguins 0.1.4, scikit-learn 1.3.0, matplotlib 3.8.0, notebook 7.4.4.


#### 4. Run the notebook

From the current directory, launch the jupyter notebook server:
```
jupyter notebook
```
This command should then point you to the right location within your browser to use the notebook, typically [http://localhost:8888/](http://localhost:8888/).

#### (Optional) Keep virtual environment persistent in jupyter Notebooks

The following step is sometimes useful if you're having trouble with your jupyter notebook finding the virtual environment. You will want to do this before
launching the jupyter notebook.
```
python -m ipykernel install --user --name=RFvenv
```


## License

The code materials in this project are licensed under the [MIT License](LICENSE).

The teaching materials are licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]


## Contribution Guidelines and Support

If you spot an issue with the materials please let us know by
[opening an issue](https://github.com/Cambridge-ICCS/RandomForests_Workshop/issues)
here on GitHub clearly describing the problem.

If you are able to fix an issue that you spot, or an
[existing open issue](https://github.com/Cambridge-ICCS/RandomForests_Workshop/issues)
please get in touch by commenting on the issue thread.

Contributions from the community are welcome.
To contribute back to the repository please first
[fork it](https://github.com/Cambridge-ICCS/RandomForests_Workshop/fork),
make the necessary changes to fix the problem, and then open a pull request back to
this repository clearly describing the changes you have made.
We will then preform a review and merge once ready.

If you would like support using these materials, adapting them to your needs, or
delivering them please get in touch either via GitHub or via
[ICCS](https://github.com/Cambridge-ICCS).
