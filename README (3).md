# PlateWise

A simulator that estimates how much lunch a school wastes and which changes are linked to less waste. Built for STEMergent Hacks 2026 (Hackathon pathway).

**Live app:** https://claude.ai/artifact/4y8UAyWwAxswHcXCnZM8Hs

## How to run
Open `index.html` in any browser. There is no build step, server or install. Fonts load from Google Fonts and fall back to system fonts offline.

## What it does
- **Simulator:** estimates waste per student per lunch from a school's traits and lunch service, and shows it against the study's primary and secondary school averages.
- **What-if comparison:** change lunch start, lunch length, milk service or waste actions and see the change.
- **Ranked changes:** each change is tagged strong or weak evidence based on statistical significance in the source paper.
- **Audit tracker:** log your own weigh-ins before and after a change. Entries are saved only in your browser.
- **Evidence page:** every coefficient, with limits.

## Data and model
Adjapong, Bender, Schaefer & Roe (2024). *School and meal characteristics associated with plate waste in K-12 cafeterias in the United States.* PLOS ONE 19(12): e0299043. CC BY 4.0. https://pmc.ncbi.nlm.nih.gov/articles/PMC11676535

The simulator uses the regression in Table 3, column 1: ln(waste, lb per student per meal) = -1.103 + sum of coefficients + 0.0286 x entrees. A coefficient c multiplies waste by e^c.

## Limits
- Observational study: results are associations, not proven effects.
- US-based, self-selected sample. Other countries may differ.
- R-squared is 0.52, so individual schools vary a lot.
- Coefficients are combined as if independent, which is approximate.
- "Outside the US" uses the average of the four US region coefficients. This is our approximation, not the paper's.
- We did not collect our own data and have not yet piloted the tool with a school.

## AI disclosure
Claude (Anthropic) helped plan the project, write the code and draft the text. [Team: edit this to say what you did yourselves.]

## Team
[Names and roles]

## Third-party resources
Google Fonts (Bricolage Grotesque, Figtree). No JavaScript libraries.
