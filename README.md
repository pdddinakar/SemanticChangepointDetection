# Semantic Changepoint Detection

This repository contains software for semantic changepoint detection and examples of its use for some of the diseases on the World Health Organization list of neglected tropical diseases, and on a corpus of literature on COVID-19.

## Viewing Results

We have already performed semantic changepoint detection analyses on the infectious diseases of Chagas Disease, COVID-19, Dengue, Echinococcosis, Leishmaniasis, Leprosy, Rabies, and Schistosomiasis. These analyses can be viewed by scrolling through the named Python Notebooks named 'Publication Analysis – {disease name}.ipynb'.

If you would like to perform the same analysis for an arbitrary disease of your choice, follow the steps in the [Installation and Usage](#installation-and-usage) section.

## Installation and Usage

1. Open a terminal window and create a folder to store the files. Here, we name the folder SemanticChangepointDetection, but you can use any name you like.

```bash
mkdir SemanticChangepointDetection
```

2. Download and save the files 'Publication Analysis — ANY DISEASE NAME.ipynb', 'requirements.txt', and 'biorxiv_covid.json' in the SemanticChagenpointDetection folder. At the end of this step, you should have the following files saved in the SemanticChangepointDetection folder.
    - Publication Analysis — ANY DISEASE NAME.ipynb
    - biorxiv_covid.json
    - requirements.txt
    
3. Download and save 'BioSentVec model 21GB (700dim, trained on PubMed+MIMIC-III)' as 'biosentvec.bin' in the SemanticChangepointDetection folder from the BioSentVec Github page available [here](https://github.com/ncbi-nlp/BioSentVec). Alternatively, the direct download link is available [here](https://ftp.ncbi.nlm.nih.gov/pub/lu/Suppl/BioSentVec/BioSentVec_PubMed_MIMICIII-bigram_d700.bin).

4. Create a Python virtual environment (any name you like, here we use env_SemanticChangepointDetection) and install the packages listed in the requirements.txt file. Install the virtual environment as a Jupyter Notebook kernel.

```bash
cd SemanticChangepointDetection
python3 -m venv env_SemanticChangepointDetection
source env_SemanticChangepointDetection/bin/activate
pip3 install -r requirements.txt
python3 -m ipykernel install --user --name=env_SemanticChangepointDetection
```

5. Open Jupyter Notebook.

```bash
jupyter notebook
```

6. In the Jupyter Notebook window, open the 'Publication Analysis — ANY DISEASE NAME.ipynb' file. Select the env_SemanticChangepointDetection kernel by clicking Kernel -> Change kernel -> env_SemanticChangepointDetection.

7. At the top of the notebook is a cell labeled 'Put your search term here and run the notebook!'. Assign your desired search term as a string for the variable ANY_DISEASE_NAME, and the run the notebook by clicking Cell -> Run All. The notebook will automatically download and analyze the publications associated with your search term using the NCBI EUtils API.
