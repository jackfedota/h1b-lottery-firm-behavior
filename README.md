# H-1B Lottery and Firm Participation

## Overview

This project examines how firms respond to outcomes in the H-1B visa lottery. Using administrative H-1B lottery data, we study whether firms that experience unexpectedly favorable lottery outcomes change their participation in subsequent lotteries.

The central question is:

**How does unexpected success in the H-1B lottery affect a firm's decision to participate and the number of registrations it submits in the following year?**

My partner, Nico Laurenson, and I conducted the project as part of SURP at California Polytechnic State University, San Luis Obispo, as assistants to our advising professor's (Joseph Kuehn) existing research project on the H-1B visa system.

## Research Question

Because H-1B visas are allocated through a lottery when demand exceeds the available supply, firms can experience selection outcomes that are better or worse than expected.

We use this variation to examine whether lottery outcomes influence firms' subsequent behavior. In particular, we analyze:

- Whether firms return to the H-1B lottery the following year
- How lottery outcomes affect the number of registrations submitted the following year
- Whether these responses depend on differing firms and worker characteristics

## Data

The analysis uses approximately **1.8 million H-1B lottery registration records** aggregated to the firm-year level from 2021-2024.

The resulting panel contains information on:

- Firm lottery registrations
- Number of selected registrations
- National lottery selection rates
- Firm-level "win" and "luck" rates
- Subsequent lottery participation
- Education characteristics of approved beneficiaries
- Firm and industry characteristics

Additional firm characteristics were incorporated using Compustat data.

## Reproducibility

The analysis files contain the code and model specifications used to produce the reported results. Because the complete H-1B datasets cannot be redistributed, the full analyses cannot be executed from the public repository alone. A small sample and reproducible demonstration are provided in `Data-Sample/` to illustrate the data structure and analytical workflow.

## Empirical Approach

## Measuring Lottery Luck

A firm's expected number of selections is calculated using its number of registrations and the national selection rate for that lottery year.

Lottery "luck" captures the difference between a firm's observed selection outcome and what would be expected based on the national selection rate.

The primary measure, `selection_luck_10pp`, expresses this selection-rate surprise in 10-percentage-point increments.

This allows us to compare firms that experienced relatively favorable or unfavorable lottery outcomes within the same lottery environment.

## Empirical Approach

The primary analysis estimates the relationship between lottery luck and subsequent firm participation.

Our main specifications examine outcomes including:

- Log next-year H-1B registrations
- Whether the firm returns to the lottery the following year

Our models control for firms' current registration volume and include lottery-year fixed effects. Standard errors are clustered at the firm level.

We also conduct heterogeneity analyses to examine whether firms respond differently depending on characteristics such as industry and the education composition of approved beneficiaries.

## Main Finding

The analysis finds that firms experiencing more favorable H-1B lottery outcomes tend to submit **fewer registrations in a following year's lottery**.

This result suggests that firms do use the H-1B lottery as intended. While some speculation exists that firms use the lottery as a substitute for cheaper labor, our results show that when labor demand gets filled, participation in future lotteries significantly declines. 
These results motivate further analysis of the mechanisms underlying this behavior.

Heterogeneity analyses explore whether this response differs across firm and worker characteristics.

## Tools

The analysis was conducted entirely in **R** and **RStudio** using a reproducible workflow.

Key tools and packages include:

- R
- tidyverse
- fixest
- ggplot
- Quarto
- Git / GitHub

## Repository Structure

The repository contains code for:

- Data cleaning and construction
- Firm-year panel creation
- Main regression analysis
- Heterogeneity analysis
- Tables and visualizations

Given the nature of our access to the H-1B data, this repository includes only a small sample of the broader dataset used in the analysis. 

## Authors

**Jack Fedota**  
B.S. Economics — Quantitative Analysis Concentration  
Statistics Minor  
California Polytechnic State University, San Luis Obispo

**Nico Laurenson**

B.S. Economics

California Polytechnic State University, San Luis Obispo

## Faculty Advisor
**Professor Joseph Kuehn**

Department of Economics

California Polytechnic State University, San Luis Obispo

