### Overview
This repo contains the code to analyze the RNA seq data in "Epigenetic dysregulation of naive CD4+ T-cell activation genes in childhood food allergy", Martino et al. 2018 (https://doi.org/10.1038/s41467-018-05608-4). 

### Data
The data was generated by profiling methylation and gene expression of naive CD4+ T cells from infants with and without egg allergy. Naive CD4+ T cells were obtained from cohort infants, stimulated, and profiled for genome-wide methylation and gene expression at age 1 (baseline) and at age 2 or 4 (follow-up), by which around 60% of infants in the allergy group had outgrown their allergy. 

The data is available on the Gene Expression Omnibus repository with the primary accession code GSE114135.


### Folder Structure
```
project
│   README.md
│   requirements.txt
├───data
│   ├───processed
│   ├───raw
│   └───results
├───fig
│   ├───main_fig
│   └───supp_fig
├───notebook
└───src
    ├───analysis
    ├───data_processing
    ├───util
    └───visualization
```
    
The purpose of the folders is as follows:
* **data/raw/**: raw data from the authors, downloaded from GEO
* **data/processed/**: intermediate data during processing
* **data/results/**: our results from our code (not yet populated in Git)
* **fig/main_fig/**: our main figures generated from our code
* **fig/supp_fig/**: our supplementary figures generated from our code (not yet populated in Git)
* **notebook/**: Jupyter notebooks for initial data visualization and exploration (not yet populated in Git)
* **src/analysis/**: code for producing results (not yet populated in Git)
* **src/data_processing/**: code for loading and processing the authors' data
* **src/util/**: helper functions and reused scripts (not yet populated in Git)
* **src/visualization/**: code for plotting results


### Installation
#### Setup
Create a virtual environment using Anaconda and navigate to that environment. Install pip:
```
conda create --name myenv
conda activate myenv
conda install pip
```

Navigate to the project directory and install the necessary packages using the requirements.txt file:
```
pip install -r requirements.txt
```

#### Running code
To generate Table 1, navigate to the main project directory and run:
```
python .\src\data_processing\process_raw_data.py
python .\src\visualization\generate_table1.py
```

"Table1.png" will be generated and stored in the folder "fig/main_fig".
