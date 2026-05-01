# DiscovAI 🔬

AI-powered drug discovery pipeline built in Python.

## What it does

DiscovAI automates the early stages of drug discovery:
- Fetches active molecules from ChEMBL (2M+ compounds database)
- Calculates physicochemical properties using RDKit
- Filters candidates with Lipinski Rule of Five
- Scores molecules on ADMET profile (Absorption, Distribution, Metabolism, Excretion, Toxicity)
- Ranks candidates with a combined DiscovAI score (60% efficacy + 40% ADMET)
- Visualizes top candidates in 2D

## Demo — BCL2 target (cancer)

BCL2 is an anti-apoptotic protein overexpressed in leukemia and lymphoma.
DiscovAI identified CHEMBL150332 as top candidate with IC50 = 13 nM and DiscovAI score = 77.8/100.

## Tech stack

- Python 3
- RDKit — molecular informatics
- ChEMBL API — pharmaceutical database
- Pandas, NumPy — data processing
- Jupyter Notebook

## Usage

```bash
conda install -c conda-forge rdkit
pip install requests pandas numpy
```

Then open `discovai_pipeline.ipynb` and run all cells.

## Author

[Maëlys Barraux] — M1 Numerical Chemistry and AI student
Université Paris cité 
