# DiscovAI

Drug discovery pipeline — Python & RDKit.

Built by a computational chemistry student tired of how slow drug discovery is.
This pipeline does in minutes what researchers do in weeks.

---

### What it does

Plug in a biological target. DiscovAI hits the ChEMBL database, pulls active molecules,
filters them through Lipinski's Rule of Five, scores each one on ADMET profile,
and ranks them by a combined efficacy + pharmacokinetics score.

Output : a ranked list of drug candidates with 2D structure visualization.

---

### Demo — BCL2 / leukemia

BCL2 is an anti-apoptotic protein overexpressed in cancer cells.
Inhibiting it restores their ability to die — the mechanism behind Venetoclax.

Top candidate identified : **CHEMBL150332**
IC50 : 13 nM — DiscovAI score : 77.8 / 100

---

### Pipeline

```
01 — Fetch molecules from ChEMBL
02 — Calculate molecular properties (MW, LogP, TPSA, HBD, HBA)
03 — Lipinski filter
04 — ADMET scoring
05 — Global ranking (60% efficacy / 40% ADMET)
06 — 2D structure visualization
```

### Stack

Python · RDKit · ChEMBL API · Pandas · NumPy · Jupyter

---

*M1 Numerical Chemistry and AI - Paris cité*
