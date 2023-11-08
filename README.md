# Direct fitting improves the accuracy of the horse radish peroxidase competition assay for peroxidase activity

### Christopher J. Barry, Ché S. Pillay, Johann M. Rohwer

Submitted to _Redox Biochemistry and Chemistry_

# Contents of this repository

This repository contains two items:

- **Supplementary code and data** to reproduce the simulations 
in the manuscript. 
- An **Excel spreadsheet template and Jupyter notebook** to perform the HRP fitting
analysis on your own data.

You can run the Jupyter notebooks *online*, or set up a *local computational environment* to 
run the simulations on your own laptop or desktop computer.

## Running the Jupyter Notebooks online

### Binder

You can use Binder to run the Jupyter Notebooks online, by clicking on this badge:  
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Rohwer-Lab/HRP-direct-fitting.git/HEAD)  
(**NOTE:** you will be directed to Binder, this will not open a new tab! You can use right-click -> `Open in new Tab`.
When the Binder environment is created for the first time, it may take a while.)
  
- This will start a JupyterLab session in your browser.
- On the left you find the folder structure. Double-click on the folder you want to open, e.g.
`Reproduce_HRP_paper_figures`. 
- The Jupyter Notebooks have a small orange image icon. Double-click on the notebook you want to run.
- Now you can interact with the notebook. To run all cells click the icon with the two arrows, left of `Download`, 
  and click on Restart in the popup.
- Each cell will automatically run from top to bottom. When a code cell was run a number appears in the brackets on the left.

**Important:** The Binder session is not persistent and any edits made to the notebooks
will be lost once the session is terminated.

### Google Colab

The `HRP_experiment_analyser` notebook, which can be used to fit your own experimental data, can additionally be
run in Google Colab - this is persistent and saved to your own Google Drive and can be done in the following steps:

- Click on the `HRP_experiment_analyser` folder.
- Click on the `HRP_experiment_analyser.ipynb` notebook file. This will display the contents of the notebook.
- Click on the ![Colab](https://colab.research.google.com/assets/colab-badge.svg) icon. This will open the
notebook in Google Colab.


## Set-up of local computational environment

Reproducing the simulations requires a working Python 3 (>=3.8, 3.11 recommended) environment 
with the Jupyter Notebook and a selection of libraries for scientific computation.
It is best set up in a **separate virtual environment** using the requirement
specifications provided, either for Anaconda, or using `pip` in a normal Python environment.

### Step 1: Clone this GitHub repository

```bash
git clone https://github.com/Rohwer-Lab/HRP-direct-fitting.git
```

### Step 2a: Install Anaconda Python distribution

By far the easiest way to set up the environment is using
[Anaconda](https://www.anaconda.com/download). Dependencies are installed automatically.
```bash
conda env create -f environment.yml
conda activate hrp-fitting
jupyter-notebook
```

### <u>OR</u> Step 2b: Install requirements using Python and `pip`

Create and activate a new virtual environment:

```bash
python -m venv hrp-fitting
source hrp-fitting/bin/activate
```

Install the requirements with:

```bash
pip install -r requirements.txt
jupyter-notebook
```

## HRP experiment analyser

To analyse your own HRP assay data with the direct fitting method:

1. Paste your raw data into the `HRP_data_template.xlsx` Excel sheet. The spreadsheet currently contains data
for demonstration purposes, which can be replaced with your own data. The sheet is annotated and 
contains further instructions.

2. Open the `HRP_experiment_analyser.ipynb` notebook in Jupyter and follow the instructions to process 
and fit the data.

## Reproduce the figures in the paper

Open the `Reproduce_HRP_paper_figures.ipynb` notebook in Jupyter. Execute the cells in sequence. 
The notebook is annotated  to explain what is being done.
