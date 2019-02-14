# Scoping discussion 2/14

### Refined proposal:

*Objective:* to predict promiscuous enzyme activity to catalyze biosynthetic reactions for which no enzyme has not yet been characterized.

*How:* build a model that predicts promiscuous activity based on machine learning training with data on known enzyme activities with chemically and structurally similar compounds

### Specs:

Databases:
- Chemical compound database
- Reaction database
    - Main enzyme activity
    - Promiscuous enzyme activity
- Enzyme database

Training data:
- Either train on existing dataset of known promiscuous enzymes OR
- Train on existing data on know primary enzyme activities

Testing data:
- 1st level: predict known activities of natural enzymes that have been left out of training data
- 2nd level: predict known promiscuous activities of enzymes

Requirements:
- Metric for chemical similarity
     - similarity index : Tanimoto, Morgan Circular Fingerprint
- Metric for rating enzyme activity
- Method for clustering enzymes based on substrate features
