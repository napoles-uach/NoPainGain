# GAINS: From PAINS to GAINS 🧪🤖
**Generative AI for No-PAIN Structures** — Repairing PAINS motifs with LLMs + RDKit

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](#)
[![RDKit](https://img.shields.io/badge/RDKit-2024.03+-brightgreen.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](#)

## Overview
**GAINS** is a lightweight, reproducible pipeline to convert PAINS (*pan-assay interference compounds*) into cleaner, drug-like candidates.  
We:
- Detect PAINS (RDKit FilterCatalog A/B/C)
- Ask an LLM to propose **minimal edits** (JSON SMILES)
- Re-evaluate candidates (QED, MW, logP, TPSA, HBD/HBA, ROT, SA)
- Export **tables + grids** comparing original vs repaired

> Key idea: instead of discarding PAINS, we **repair** them — turning **PAINS → GAINS**.

## Demo
- **Colab (GPT-only pipeline):** _add your link here_  
- **Colab (ChEMBL → PAINS → LLM):** _add your link here_  
- **Slides / 2-min video:** _add your link here_

## Repo structure
```
.
├── notebooks/
│   ├── 01_chembl_to_pains.ipynb
│   ├── 02_llm_edits_eval.ipynb
│   └── 03_compare_orig_vs_gpt.ipynb
├── data/
│   ├── pains_chembl.csv
│   ├── pains_chembl_eval.csv
│   └── chembl_fixes_gpt.csv
├── figures/
│   ├── chembl_pains_grid.png
│   ├── gpt_grid.png
│   └── compare_grid.png
├── scripts/                # (optional) helper scripts
└── README.md
```

## Quickstart

### Option A — Colab (recommended)
1. Open the Colab notebook  
2. Set your API key:
```python
import os
os.environ["OPENAI_API_KEY"] = "sk-..."
```
3. Run all cells. Outputs will include:
- `pains_chembl.csv`, `pains_chembl_eval.csv`
- `chembl_fixes_gpt.csv`
- `chembl_pains_grid.png`, `gpt_grid.png`, `compare_grid.png`

### Option B — Local
```bash
# create env
python -m venv .venv && source .venv/bin/activate
pip install -U pip

# dependencies
pip install rdkit-pypi pandas openai chembl_webresource_client

# set key
export OPENAI_API_KEY=sk-...

# run notebooks manually or adapt as scripts
```

## Reproducibility: end-to-end
1. **Download PAINS from ChEMBL**  
   - `chembl_webresource_client` → filter by MW, sanitize SMILES, apply **RDKit PAINS A/B/C**  
   - save **`pains_chembl.csv`**  
2. **Evaluate originals**  
   - compute QED, MW, logP, TPSA, HBD/HBA, ROT → **`pains_chembl_eval.csv`**  
   - generate **`chembl_pains_grid.png`**  
3. **LLM proposals**  
   - prompt model (e.g. `gpt-4o-mini`) for *minimal edits* (strict JSON)  
   - sanitize, re-evaluate PAINS + properties → **`chembl_fixes_gpt.csv`**  
   - grid **`gpt_grid.png`** (top non-PAINS)  
4. **Compare**  
   - merge original vs proposal by `chembl_id` (`parent`)  
   - side-by-side grid **`compare_grid.png`**  
5. **(Optional)** SA score + multi-objective ranking  
   - `score = QED - 0.02*ROT - 0.1*SA`

## Key files
- **Data**
  - `data/pains_chembl.csv` — PAINS molecules from ChEMBL (ID + SMILES + motif)
  - `data/pains_chembl_eval.csv` — originals with properties
  - `data/chembl_fixes_gpt.csv` — GPT-proposed evaluated molecules
- **Figures**
  - `figures/chembl_pains_grid.png` — PAINS examples
  - `figures/gpt_grid.png` — top repaired candidates
  - `figures/compare_grid.png` — before/after comparisons

## Prompt (LLM)
> *You are a medicinal chemist… propose N minimally edited variants (SMILES only) that remove the PAINS substructure… Return ONLY a valid JSON array of objects with key "proposal". Soft constraints: 200≤MW≤500, 0≤logP≤4.*

_(see notebook for the full version)_

## Why it’s different
- We don’t just filter PAINS: **we repair them** with minimal AI-guided edits.  
- Transparent, auditable pipeline with RDKit.  
- Ready for hackathons / PoC, extensible (BRENK, SMARTS rules, ADMET).  

## Cite
If you use GAINS in a project/publication, please cite this repo.  
_Add CITATION.cff or BibTeX here._

## License
MIT (or your preferred license).  
_Add LICENSE file._

## Acknowledgements
- ChEMBL (EBI), RDKit, OpenAI.  
- Inspired by PAINS literature (Baell & Holloway, 2010).

