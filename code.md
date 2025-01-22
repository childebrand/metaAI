---
title: Code
nav_order: 4
layout: home
---

# Download Meta Analysis R Code

This repository contains the complete R Markdown file used for our meta-analysis on AI resistance across markets. The file includes all data preprocessing steps, effect size calculations, and visualizations presented in the paper.
Getting Started
Download the R Markdown file below to reproduce our analysis:

## 📥 Download metaanalysis.Rmd
The R Markdown file contains main set of analyses, including comments explaining the code and main insights of each analysis.

Download the file here:


### Number of Effect Sizes by Authors
```{r s_by_authors_I, include=FALSE}
authors_plotdata <- meta_data %>%
        group_by(authors_short) %>%
        dplyr::summarize(n = n()) %>% 
        dplyr::mutate(pct = n/sum(n),
                      lbl = scales::percent(pct)) %>% 
        arrange(desc(pct))

authors_plotdata$authors_short <- as.factor(authors_plotdata$authors_short)
plot_by_authors <- ggplot(authors_plotdata, aes(x = reorder(authors_short, n), y = n)) +
        geom_bar(stat = "identity")+
        geom_text(aes(label = n, hjust = -0.1))+
        coord_flip()+
        theme_bw()+
        labs(x = "", y ="")
```
