---
title: Data
layout: home
nav_order: 3
---

# Meta-Analysis Dataset 

Download our complete dataset of AI resistance effects:

[📥 Download metaanalysis_data.csv](meta_docs/metaanalysis_data.csv) 

## Dataset Overview

The dataset contains:
- 🤖 Effect sizes and standard errors for AI labels / types, AI Characteristics
- 📚 Study characteristics (e.g., participant pool, incentive compatibility, etc.)
- 🏢 Application domains (e.g., finance, healthcare, transporation, etc.)
- 📅 Study periods

Each row represents one effect size, with columns following the [PRISMA-IPD](http://prisma-statement.org) reporting guidelines.

## Data Dictionary

Important variables:
```r
names(data)
[1] "es_id"            # Effect size ID 
[2] "ai_label"         # How AI was described to participants
[3] "cohens_d"         # All effect sizes converted to Cohen's d
[4] "p_value"          # Exact p-values reported where possible
[5] "n"                # Total sample size of a study
[6] "n1 / n2"          # Number of observations / samples per condition
```

Please cite our paper when using this dataset:
```bibtex
@article{zehnle2025meta,
  title={Not All AI Is Created Equal: A Meta-Analysis Revealing Drivers of AI Resistance Across Markets, Methods, and Time},
  author={Zehnle, Meike and Hildebrand, Christian and Valenzuela, Ana},
  journal={International Journal of Research in Marketing},
  year={2025},
  volume={xx},
  number={xx},
  pages={xx},
  doi={10.xxxx/xxxxx}
}
```


