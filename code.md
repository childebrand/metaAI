---
title: Code
nav_order: 4
layout: home
---

# Download Meta-Analysis R Code

This repository contains the complete R Markdown file used for our meta-analysis on AI resistance across markets. The file includes all data preprocessing steps, analyses, and visualizations presented in the paper.

## Getting Started
Download the R Markdown file(s) below to reproduce our analyses:

## 📥 Download Code
The R Markdown file contains all main analyses presented in our meta-analysis.

- Analysis Code: [📥 Download metaanalysis.Rmd](meta_docs/metaanalysis.Rmd) 

### Exemplary Sample Code (here: comparison of effect sizes across ai label categories)
```r 
ai_robots <- metafor::rma.mv(cohens_d, variance_d, mods = ~ relevel(factor(ai_label), ref = 'ai robots'), data = df, random = ~ 1 | article_id/es_id, tdist = TRUE, btt = 2:4)
ai_robots_robust <- robust(ai_robots, cluster = study_id)

# AI label plot.
coef_order <- coef(ai_label_robust)
ai_label_plot <- df %>%
	  filter(!is.na(ai_label)) %>%
	  mutate(ai_label = fct_recode(fct_reorder(ai_label, coef_order[paste0("factor(ai_label)", ai_label)], .desc = TRUE),
	                               "AI Algorithms" = "ai algorithms",
	                               "AI Systems" = "ai systems",
	                               "AI Assistants" = "ai assistants",
	                               "AI Robots" = "ai robots")) %>%
	  ggplot(aes(x = ai_label, y = cohens_d)) +
	  geom_violin(trim = FALSE, fill = blue_light, color = blue_dark) +
	  geom_boxplot(width = 0.1, fill = blue_medium, color = blue_dark, 
	               outlier.shape = NA) +
	  stat_summary(fun = median, geom = "point", shape = 21, size = 2,
	               fill = "white", color = "black") +
	  geom_hline(yintercept = 0, linetype = "dashed", size = 1, 
	             color = red_line) +
	  scale_y_continuous(limits = c(-3, 2), breaks = seq(-3, 2, 1)) +
	  labs(x = "AI Label", y = "Cohen's d") +
	  theme_classic() +
	  theme
```
