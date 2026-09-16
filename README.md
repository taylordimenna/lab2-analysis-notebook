# Lab 2 Analysis Notebook
Contains my work for Lab 2: Analysis Notebook

## Project Overview
This project analyzes RNA-sequencing data from human airway smooth muscle cells using the GEO GSE52778 dataset. The analysis explores how different asthma treatments are associated with differences in gene expression.

### Research Question
How do different asthma treatments affect gene expression in human airway smooth muscle cells?

### Treatment groups
This analysis compares four different asthma treatment groups:
- Dexamethasone
- Albuterol
- No treatment
- Dexamethasone + Albuterol

### Dataset
The dataset is the "Human Airway Smooth Muscle Transcriptome Changes in Response to Asthma Medications" from the NCBI Gene Expression Omnibus (GEO), accession GSE52778.

It is loaded directly from the NCBI GEO download URL. No manual download is needed.

URL:
https://www.ncbi.nlm.nih.gov/geo/download/?acc=GSE52778&format=file&file=GSE52778_All_Sample_FPKM_Matrix.txt.gz

## Setup
### 1. Clone the repository
Make a copy of this repository to your local computer.

Run the following command:

    git clone https://github.com/taylordimenna/lab2-analysis-notebook.git

### 2. Move into repository
Run the following command:

    cd lab2-analysis-notebook

You are now inside the ```lab2-analysis-notebook``` directory.

## Python Setup
### 1. Verify Python
Python version 3 is required. To check and confirm that Python is available, run the following command:

    python --version

### 2. Download required packages
The following packages are required for the notebook:
- pandas
- numpy
- matplotlib
- scikit-learn
- jupyter
- nbconvert

These packages need to be installed for the Python Notebook to run. 

To install them, run the following command within the VS Code Terminal:

    python -m pip install pandas numpy matplotlib scikit-learn jupyter nbconvert

This will download them all at once.

## R Setup
R 4.5.1 and RStudio were used to create and run the R Notebook.

The following packages are required for the notebook:
- readr
- dplyr
- ggplot2
- rmarkdown

These packages need to be installed for the R Notebook to run.

To install them, open RStudio and run the following command:

    install.packages(c("readr", "dplyr", "ggplot2", "rmarkdown"))

## Run the Python Notebook
### 1. Open the notebook
If you're using Jupyter directly, run:

    jupyter notebook

And open ```python_notebook.ipynb```.

If you're using VS Code, open the cloned ```lab2-analysis-notebook``` folder and open  ```python_notebook.ipynb```.

### 2. Run the analysis
In the notebook:
1. Restart the kernel.
2. Run all cells
3. Confirm that all cells were executed without errors.

## Run the R Notebook
### 1. Open the R project
Open ```lab2-analysis-notebook.Rproj``` in RStudio.

This opens the repository as an RStudio project.

### 2. Open the R Notebook
Open ```r_notebook.Rmd``` in RStudio.

### 3. Run the analysis
In the RStudio Console, run the following command:

    rmarkdown::render("r_notebook.Rmd")

This produces ```r_notebook.html```, which contains the rendered output in HTML form.

## Run Data Fetch Script
```fetch_data.py``` retrieves the original dataset (GSE52778) directly from NCBI GEO.

In the repository directory, run the following command:

    python fetch_data.py

The script should produce an output similar to:

    Data loaded successfully: 23273 rows x 41 columns

## Render the Python Notebook to HTML
To generate the HTML version of the Python notebook, from the repository directory run the following command:

    python -m jupyter nbconvert --to html python_notebook.ipynb

This produces ```python_notebook.html```, which contains the rendered output in HTML form.

## Repository Contents
```.gitignore``` contains the files that should not be committed to the repository.

```AI_USAGE.md``` contains information about any AI tools used to help complete this lab.

```fetch_data.py``` contains a script that fetches the source data.

```lab2-analysis-notebook.Rproj``` is the RStudio project file for the repository.

```python_notebook.html``` contains the HTML rendered output for the ```python_notebook.ipynb``` Jupyter notebook.

```python_notebook.ipynb``` contains the Jupyter notebook that loads the data, performs a transformation/analysis, produces a visualization to address the research question. The Graduate Addendum is located here.

```r_notebook.Rmd``` contains the R Notebook that performs the sama analysis as ```python_notebook.ipynb``` just using R. The Graduate Addendum is located here.

```r_notebook.html``` contains the HTML rendered output for the ```r_notebook.Rmd``` R notebook.