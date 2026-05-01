# DiscovAI

Drug discovery pipeline — Python & RDKit.

Automates early-stage molecular screening against a biological target.
Built as part of a computational chemistry research project.

## What it does

Connects to ChEMBL, the world's largest open bioactivity database,
and runs a full screening pipeline on any target of interest.

- Molecular property calculation
- Lipinski drug-likeness filter
- ADMET scoring — absorption, distribution, metabolism, excretion, toxicity
- Global candidate ranking combining efficacy and pharmacokinetic profile
- 2D structure visualization of top candidates

## Demo

Target : BCL2 — anti-apoptotic protein involved in leukemia and lymphoma  
Top candidate : CHEMBL150332  
IC50 : 13 nM  
DiscovAI score : 77.8/100  

## Stack

Python — RDKit — ChEMBL API — Pandas — NumPy

## Usage

```bash
conda install -c conda-forge rdkit
pip install requests pandas numpy
```

Open `discovai_pipeline.ipynb` and run.

## Author

[Maëlys Barraux] — M1 Numerical Chemistry and AI student
Université Paris cité 
