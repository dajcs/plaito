# PLAITO
Exercise for Requirements Engineering (PLAITO Project)

## Tasks
1. **Manual Summary:**  
Making a manual summary of the paper **An empirical study on the potential usefulness of domain models for completeness checking of requirements** by Chetan Arora, Mehrdad Sabetzadeh and Lionel C. Briand. (https://doi.org/10.1007/s10664-019-09693-x).  
This summary is saved in a file named [MySummary.docx](./MySummary.docx) and can be viewed at [MySummary.pdf](./MySummary.pdf).  
In order to allow automatic processing, this summary has been saved in text format with `UTF-8` encoding in file [MySummary.txt](./MySummary.txt).

2. **LLM-Generated Summary:**  
Using the ChatGPT 4o model web interface to generate a summary by attaching the pdf version of the paper and providing the prompt:  
`Can you make a 3 page long summary of the attached paper?  
Please make a detailed summary, capture the essence and provide sufficient detail to stand alone for readers unfamiliar with the original document.`  
The generated summary is copy/pasted and saved into [LLM_Summary.docs](./LLM_Summary.docx) file and can be viewed at [LLM_Summary.pdf](./LLM_Summary.pdf).  
The `UTF-8` encoded text version is saved into the [LLM_Summary.txt](./LLM_Summary.txt) file.

3. **Automated Analysis Script:**  
The notebook script [summary_comp.ipynb](./summary_comp.ipynb) performs:
   - **Clustering:** organizing each summary into predefined themes (e.g. context, problem statement)
   - **Comparison:** comparing the clustered results  

    **Setup:** For this exercise the Python v3.11 has been used with [conda](https://www.anaconda.com/docs/getting-started/miniconda/install). The file [requirements.yml](./requirements.yml) contains packages for `jupyter lab` and clients for major language models and for [huggingface](https://huggingface.co/) (the github for LLMs).  
    These are the commands to create new environment called `plaito`, to activate it, and start jupyter lab:
    ```
    conda update conda
    conda env create -f environment.yml
    conda activate plaito
    jupyter lab
    ```  
    Alternatively the packages can be installed without `conda` in a Python environment using the file [requirements.txt](requirements.txt) with command:  
    ```
    pip install -r requirements.txt
    ```

4. **Optional Challenge - DeepSeek Summary:**
We made another summary of the original study on the [DeepSeek](https://chat.deepseek.com/) web interface with the R1 model.  
The initial prompt
    ```
    Can you make a 3 page long summary of the attached paper? Please make a detailed summary, capture the essence and     provide sufficient detail to stand alone for readers unfamiliar with the original document.
    ```
    provided us with a 2 page long summary, but it was "thinking" that it provided us a  
    `Word Count: ~1,200 (≈3 pages)` long summary.
    
    On the second prompt we tried to persuade to make the summary somewhat longer:
    ```
    My wordcount resulted in 674 words (2 pages).  Can you put some more details in it to have 1000+ words?
    ```
    
    The resulting summary has been saved as [DS_Summary.docx](./DS_Summary.docx) and it can be viewed at [DS_Summary.    pdf](./DS_Summary.pdf).  
    The text version is saved with `UTF-8` encoding at [DS_Summary.txt](./DS_Summary.txt)

5. **Comparative Analysis Findings**  
The findings on comparative analysis of human and LLM generated summaries can be read in the [Comparative_Analysis_Findings.pdf](./Comparative_Analysis_Findings.pdf) document.