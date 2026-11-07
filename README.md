# Customer Decision Analytics

An end-to-end analysis showing how customer data can answer four connected business questions: what to build, what to charge, what actually works, and how to prove it. It combines choice modeling, causal inference, positioning analysis and marketing measurement into a single recommendation.

**Case study:** a consumer app launching a new subscription line-up.

## What this project demonstrates

| Business question | Method | Capability shown |
|---|---|---|
| What do customers value, and what will they pay? | Choice-based conjoint, conditional logit, willingness to pay, segment models | Turning survey choices into pricing and product decisions |
| Did the offer cause more upgrades, or did it reach people who would upgrade anyway? | Propensity scores, IPW, doubly robust AIPW, balance and sensitivity checks | Causal inference from non-randomized data |
| Which products compete, and where is the gap? | Multidimensional scaling, Gower distance, constrained candidate search, line-up simulation | Translating data into positioning and product strategy |
| Which marketing channels work, and how can we know? | Ridge marketing mix model, adstock, block bootstrap, placebo tests, experiment sizing | Honest measurement and experiment design |

## Why the analysis can be trusted

- **Tested against simple alternatives:** forecasts are compared with naive benchmarks on held-out weeks. The marketing model did not significantly beat trend and seasonality on any outcome, and the analysis reports that. The conjoint is checked against the choices it was fitted on.
- **Uncertainty is reported:** key estimates carry confidence intervals from bootstrap methods suited to each data structure.
- **Assumptions are challenged:** overlap, balance, sensitivity and placebo checks try to break each conclusion.
- **Limits are stated plainly:** the marketing model did not support moving budget, so the analysis says so and designs the experiments that would answer the question.

## Outcome

The analysis recommends a three-tier line-up led by a refined \$12 bundle, refining the offer before scaling it, and holding channel budgets until experiments can measure each channel. A sequenced test plan with decision rules sets out what would confirm or overturn each recommendation.

## Explore the analysis

The full analysis, including concept explanations for each method, is in [customer_decision_analytics.ipynb](customer_decision_analytics.ipynb). It opens with an executive summary and runs end to end from the data files in this repository.

**Tools:** Python, pandas, statsmodels, scikit-learn, SciPy, matplotlib.
