# anaconda-notes
Notes on Anaconda

## [freelearning.anaconda.cloud](https://freelearning.anaconda.cloud/)

### [What are Modules, Packages, and Libraries?](https://freelearning.anaconda.cloud/get-started-with-anaconda/19826):

@01:13:
Tools

Data Analysis
- pandas
- NumPy
- SciPy

Machine Learning
- TensorFlow
- scikit learn
- PyTorch
- Keras

Data Visualization
- matplotlib
- bokeh
- plotly
- Streamlit

### [Understanding Conda](https://freelearning.anaconda.cloud/get-started-with-anaconda/19308):

conda: an open-source tool for managing:
- package:
  - repositories
  - dependencies
and
- environments
for all programming languages:
- Python
- R
- Ruby
- Lua
- Scala
- Java
- JavaScript
- C/C++
- FORTRAN

@00:21:

A cooking analogy:
- conda like a kitchen
- has pantry - store `utensils, appliances, ingredients`
- in conda - package repository acts like a pantry
- where instead of `utensils, appliances, ingredients` you find softwaree programs known as packages.

- a dish depends on utensils and ingredients
- in conda each package may depend on other packages
- e.g. when install package: pandas, automatically install other packages that depends on like NumPy.

@01:13: 

- packages are like recipies
- you may use one prepared by someone else with recipe and ingredients. -> reproducible meal
- in Anaconda environments act like meal kits
- create a reproducible environment from an environment.yml file you or others created
- can pin versions of packages in environment.

@01:51:
Recommended: Create separate environments per project

Environment management:
- environment each for:
  - ML/AI Project
  - ETL dashboarding project
  - R project

### [Conda Workflow: Creating Environments, Installing Packages, and Launching an IDE](https://freelearning.anaconda.cloud/get-started-with-anaconda/18202)

@00:18:

#### A Conda Workflow:

1. create environment
2. activate environment
3. install packages
4. launch JupyterLab
5. deactivate environment

@00:34:
1. Create environment

on Windows: open `anaconda prompt`
```bash
conda --version
```

```bash
conda env list
```

- you always begin in base environment
- always create a new environment
- never work in base

@01:07

```bash
conda create --name example
```

can create environment with a specific version of python:

e.g. :

```bash
conda create --name examnple python=3.9
```

@01:41

2. Activate Environment

moves you out of `base` into -> new environment e.g. `example`
- here you can install separate
- distinct versions of python
- and packages
- specifically for your project
- without affecting `base` environment packages.

Rerun:

```bash
conda env list
```

ensure new environment: `example` is in your environment list

@02:04:

to activate:

```bash
conda activate example
```

@02:12:

once in new environment:

```bash
conda list
```

3. install packages

to see installed packages

can install multiple packages in one command:

e.g. :

```bash
conda install jupyterlab dask pandas hvplot
```

@02:35:

If you cannot find a package on
`the default conda channel`
you can search for it on:
[anaconda.org](https://anaconda.org/)
where robust channels like conda forge host
many additional packages

@02:45

to install a package from

`conda forge`

for example

add 

```bash
-c
```

to the channel name

e.g. :

```bash
conda install -c conda-forge conda-stats
```

4. launch jupyterlab

```bash
jupyter-lab
```

@03:20 to @03:30

working in jupyter-lab in browser example

@03:30:

to end jupyter lab session:

`Ctrl + C`

@03:44:

5. deactivate environment

Best practice:
Deactivate environment before switching to another environment
- once working with multiple projects

@03:52:

```bash
conda deactivate
```

[What is an IDE?](https://freelearning.anaconda.cloud/get-started-with-anaconda/36655) :

- IDE Integrated Development Environment
- Python IDE's
