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
- Train on existing data on known primary enzyme activities

Testing data:
- 1st level: predict known activities of natural enzymes that have been left out of training data
- 2nd level: predict known promiscuous activities of enzymes

Validation:
- compare with native pathways e.g) GTP to folate 
- compare with unnatural but reported pathway  

Requirements:
- Metric for chemical similarity
     - similarity index : Tanimoto, Morgan Circular Fingerprint
- Metric for rating enzyme activity
- Method for clustering enzymes based on substrate features

--------

Databases
- see the previous list

Finding known enzymes
- create a tool that interacts w/ GUI of KEGG

Input
- target compound, starting compound
- we need a starting and ending compound to clearly define what type of chemical rxn it is- then you can find similar rxns
- single step reactions at first- will be able to chain single steps in the future

Output
- pathway with known enzymes, putative pathways ranked on likelihood

Define substrate and product scope 
- what would be an example of a compound we would use - *a priori* selection
- biosynthetic routes (e.g. rapamycin, shikimate pathway), one that isn't known 
- CARs? 

How to measure chemical similarity? 
- based on enzyme structure? (no!)
- based on the chemicals that the enzyme can transform
- tanimoto similarity index

What tool are we using to measure similarity?
- RDKit
- ML to group or cluster enzymes by some similarity cutoff- use features as predictors for novel activity (SVMs?)

ATLAS gives us scope -separates rxns that have known enzymes vs those that don't- allows us to find the novel rxns
- expands the number of enzymes we have to select from (putative enzymes)

## NEED
- good dataset with promiscuous activities
- Tyo lab - not much data on promiscuity - very few enzymes have more than twenty substrates
- first find group of enzyme (e.g. oxidation), then find enzyme that matches the substrate (change carboxylic acid to alcohol- the other part of the molecule will be recognized by enzyme) - two steps- find enzyme that recognizes the functional group, find substrate scope of those enzymes. 
:- search for intersection of groups 
