---
title: Data
layout: home
nav_order: 3
---

# Meta-Analysis Dataset 📊

Download our complete dataset of AI resistance effects across markets:

[📥 Download data.xlsx](meta_docs/data.xlsx) 

## Dataset Overview

The dataset contains:
- 🔢 Effect sizes and variances
- 📚 Study characteristics
- 🏢 Market categories
- 📅 Study periods
- 🤖 AI system types

Each row represents one effect size, with columns following the [PRISMA-IPD](http://prisma-statement.org/Extensions/IndividualPatientData) reporting guidelines.

## Data Dictionary

Key variables:
```r
names(data)
[1] "study_id"      # Unique identifier for each study
[2] "effect_size"   # Hedges' g
[3] "variance"      # Effect size variance
[4] "market_type"   # B2C, B2B, or mixed
[5] "ai_type"       # Type of AI system studied
[6] "sample_size"   # Total sample size
[7] "year"          # Publication year
```

Please cite our paper when using this dataset:
```bibtex
@article{childebrand2025ai,
  title={Not All AI Is Created Equal: A Meta-Analysis Revealing Drivers of AI Resistance Across Markets, Methods, and Time},
  author={Childebrand, et al.},
  year={2025}
}
```


