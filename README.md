# Protein-Identifier
This python code works on jupyter notebook.

# Project Title: Protein-Identifier

A Jupyter Notebook workflow designed to take raw nucleotide sequences, translate them into amino acids, and identify the corresponding proteins using NCBI BLAST.

## 📌 Project Overview
* **What is the goal of this project?**
* Using BLAST homology searches to try to identify an unknown DNA sequence. 
* **Why is this project useful?**
* Translate a nucleotide sequence to protein by running BLAST searchesn with the BLAST module in Biopython
* **What dataset or input sequence does this focus on?**
* Cell division protein FtsZ [Pseudomonas aeruginosa]

## 🧬 Biological Workflow
Briefly explain the pipeline steps implemented in your notebook:
1. **Input**: Reading a raw nucleotide sequence file named Mystery_Gene.txt
2. **Translation**: Translating the nucleotide sequence to RNA sequence. Then, translating the RNA sequence to codon list. At last, translating the codon list to an amino acids strings
3. **Identification**: Submitting protein strings via `NCBIWWW.qblast` to the Non-Redundant (`nr`) database
4. **Output**: Exporting top organism matches and E-values 

## 🛠️ Installation & Setup

### Prerequisites
Make sure you have the following software installed:
* Python 3.14.5
* Jupyter Notebook or JupyterLab

### Required Libraries
To run this notebook, you need to install the following dependencies. Run this command in your terminal:
```bash
pip install numpy pandas matplotlib biopython
```

## 🚀 How to Run the Notebook
1. Clone this repository or download the `protein-identifier.ipynb` file.
2. Place the Mystery-Gene.txt sequence files in the `/data` directory. 
3. Open your terminal and start Jupyter: `jupyter notebook`.
4. Open `protein-identifier.ipynb` and run the cells sequentially.

## 📊 Sample Results
* **Top Hit Identified**: Cell division protein FtsZ [Pseudomonas aeruginosa]
* **E-value / Confidence**: 0.0
* **Visualizations Included**:
*  'ref|WP_011666751.1| cell division protein FtsZ [Pseudomonas aeruginosa] >gb|ABJ15653.1| cell division protein FtsZ [Pseudomonas aeruginosa UCBPP-PA14]'
* Sequence: ref|WP_011666751.1| cell division protein FtsZ [Pseudomonas aeruginosa] >gb|ABJ15653.1| cell division protein FtsZ [Pseudomonas aeruginosa UCBPP-PA14]
* length: 394
* e value: 0.0

## ⚠️ Important Considerations / Limitations
* **Internet Dependence**: The notebook uses the online NCBI BLAST API (`NCBIWWW.qblast`). Large batches of sequences may take a long time to run or risk being throttled by NCBI servers. 

## 👥 Authors & Acknowledgments
* **Author**: Tik YuenWah Wong
* **Acknowledgments**: Thanks to Biopython developers / NCBI BLAST services / CalTach IPBR Coding Course: Introduction to Programming for Biological Research
