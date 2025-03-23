# PLAITO
Exercise for PhD Candidates in Requirements Engineering (PLAITO Project)

## Tasks
1. **Manual Summary:**  
Making a manual summary of the paper **An empirical study on the potential usefulness of domain models for completeness checking of requirements** by Chetan Arora, Mehrdad Sabetzadeh and Lionel C. Briand. (https://doi.org/10.1007/s10664-019-09693-x).  
This summary is saved in a file named [MySummary.docx](./MySummary.docx).  
In order to allow automatic processing, this summary has been saved in text format with `UTF-8` encoding in file [MySummary.txt](./MySummary.txt).

2. **LLM-Generated Summary:**  
Using the ChatGPT 4o model web interface to generate a summary by attaching the pdf version of the paper and providing the prompt:  
`Can you make a 3 page long summary of the attached paper?  
Please make a detailed summary, capture the essence and provide sufficient detail to stand alone for readers unfamiliar with the original document.`  
The generated summary is copy/pasted and saved into [LLM_Summary.docs](./LLM_Summary.docx) file.  
The `UTF-8` encoded text version is saved into the [LLM_Summary.txt](./LLM_Summary.txt) file.

3. **Automated Analysis Script:**  
The notebook script [summary_comp.ipynb](./summary_comp.ipynb) performs:
   - **Clustering:** organizing each summary into predefined themes (e.g. context, problem statement)
   - **Comparison:** comparing the clustered results  

    **Setup:** For this exercise the Python v3.11 has been used with [conda](https://www.anaconda.com/docs/getting-started/miniconda/install). The file [requirements.yml](./requirements.yml) contains packages for `jupyter lab` and clients for major language models and for [huggingface](https://huggingface.co/) (the github for LLMs)  
    The commands to create new environment called `plaito`, activate, and start jupyter lab:
    ```
    conda update conda
    conda env create -f environment.yml
    conda activate plaito
    jupyter lab
    ```  
    Alternatively the packages can be installed from the file [requirements.txt](requirements.txt) a Python environment without `conda` with command:  
    ```
    pip install -r requirements.txt
    ```

