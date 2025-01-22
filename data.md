---
title: Data
layout: home
nav_order: 3
---

# Meta-Analysis Dataset 

Download our complete dataset of AI resistance effects:

[📥 Download data.xlsx](meta_docs/data.xlsx) 

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
[1] "study_id"         # Unique identifier for each study
[2] "es_id"            # Effect size ID 
[3] "cohens_d"         # All effect sizes converted to Cohen's d
[4] "ai_terminology"   # How AI was described to participants
[5] "m_human"          # Arithmetic mean of human condition
[6] "m_ai"             # Arithmetic mean of AI condition
[7] "final_study_n"    # Total sample size
[8] "pubyear"          # Publication year
```

Please cite our paper when using this dataset:
```bibtex
@article{
  title={Not All AI Is Created Equal: A Meta-Analysis Revealing Drivers of AI Resistance Across Markets, Methods, and Time},
  author={Zehnle, Hildebrand, Valenzuela},
  year={2025}
}
```


