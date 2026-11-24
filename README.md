# Micro-market segmentation of tiendas de abarrotes (Mexico City metro area)

Unsupervised learning project that groups the traditional grocery stores (*tiendas de abarrotes*) of
Mexico City and the Valley of Mexico metropolitan area (ZMVM) into actionable micro-market segments,
using public INEGI data, to help a wholesaler prioritise clients, plan routes, tailor assortment and
identify expansion zones.

- **Task:** clustering (K-Means, Hierarchical, DBSCAN)
- **Primary metric:** silhouette score (plus Davies–Bouldin, Calinski–Harabasz, stability and a fairness check)
- **Data:** INEGI DENUE (business directory), 2020 Population and Housing Census (AGEB level),
  CONAPO 2020 urban marginalization index

## Project structure

```
├── config.yaml          # region, radius, paths, random seed (change the region here to scale)
├── requirements.txt
├── data/
│   ├── raw/             # INEGI downloads (not committed)
│   ├── interim/
│   └── processed/
├── notebooks/           # exploration and reporting notebooks
├── src/
│   ├── data/            # download and loading scripts
│   ├── features/        # feature engineering
│   ├── models/          # clustering training and evaluation
│   └── viz/             # maps and plots
├── models/              # saved models and configs
└── reports/
    ├── figures/
    └── 01_problem_framing.md
```

## How to reproduce

First time only (Anaconda Prompt):

    conda create -n capstone python=3.12 -y
    conda activate capstone
    pip install -r requirements.txt

Every session:

    cd <path to this repo>
    conda activate capstone
    jupyter lab

1. `pip install -r requirements.txt`
2. Review `config.yaml` (region, competition radius, random seed)
3. `python -m src.data.download` → `python -m src.features.build_features` → `python -m src.models.train_clustering`
   *(scripts are added as the project progresses)*

## Status

Work in progress — capstone project, Postgraduate Programme in Data Science & AI (December 2026).
