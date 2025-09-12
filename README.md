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
├── scripts/                # (opcional) helpers .py
└── README.md
```

## Quickstart

### Option A — Colab (recommended)
1) Abre el notebook de Colab  
2) Configura tu clave:
```python
import os
os.environ["OPENAI_API_KEY"] = "sk-..."
```
3) Ejecuta todas las celdas. Se guardarán:
- `pains_chembl.csv`, `pains_chembl_eval.csv`
- `chembl_fixes_gpt.csv`
- `chembl_pains_grid.png`, `gpt_grid.png`, `compare_grid.png`

### Option B — Local
```bash
# create env
python -m venv .venv && source .venv/bin/activate
pip install -U pip

# deps
pip install rdkit-pypi pandas openai chembl_webresource_client

# set key
export OPENAI_API_KEY=sk-...

# run notebooks (manual) o convierte a script si quieres
```

## Reproducibility: end-to-end
1) **Download PAINS from ChEMBL**
   - `chembl_webresource_client` → filtra por MW, sanitiza SMILES, aplica **RDKit PAINS A/B/C**
   - guarda **`pains_chembl.csv`**  
2) **Evaluate originals**
   - calcula QED, MW, logP, TPSA, HBD/HBA, ROT → **`pains_chembl_eval.csv`**
   - genera **`chembl_pains_grid.png`**
3) **LLM proposals**
   - prompta el modelo (ej. `gpt-4o-mini`) para *minimal edits* (JSON estricto)  
   - sanitiza, re-evalúa PAINS + propiedades → **`chembl_fixes_gpt.csv`**
   - grilla **`gpt_grid.png`** (top no-PAINS)
4) **Compare**
   - une original vs propuesta por `chembl_id` (`parent`)  
   - grilla lado a lado **`compare_grid.png`**
5) **(Optional)** SA score + ranking multi-objetivo  
   - `score = QED - 0.02*ROT - 0.1*SA`

## Key files
- **Data**
  - `data/pains_chembl.csv` — PAINS reales de ChEMBL (ID + SMILES + motivo)
  - `data/pains_chembl_eval.csv` — originales con propiedades
  - `data/chembl_fixes_gpt.csv` — propuestas GPT evaluadas
- **Figures**
  - `figures/chembl_pains_grid.png` — ejemplos PAINS
  - `figures/gpt_grid.png` — top candidatos reparados
  - `figures/compare_grid.png` — antes/después

## Prompt (LLM)
> *You are a medicinal chemist… propose N minimally edited variants (SMILES only) that remove the PAINS substructure… Return ONLY a valid JSON array of objects with key "proposal". Soft constraints: 200≤MW≤500, 0≤logP≤4.*

_(ver notebook para la versión completa)_

## Why it’s different
- No solo filtramos PAINS: **los reparamos** con ediciones mínimas guiadas por IA.  
- Pipeline auditable con RDKit; resultados transparentes (CSV + PNG).  
- Listo para hackathons / PoC y extensible (BRENK, reglas SMARTS, ADMET).

## Cite
If you use GAINS in a project/publication, please cite this repo.  
_Add CITATION.cff or BibTeX here if deseas._

## License
MIT (o la que prefieras).  
_Add LICENSE file._

## Acknowledgements
- ChEMBL (EBI), RDKit, OpenAI.  
- Proyecto inspirado por la literatura PAINS (Baell & Holloway, 2010).
