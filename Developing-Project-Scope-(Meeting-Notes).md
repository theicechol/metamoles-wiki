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

-------

## 2/21/19 *Proposal: Limiting Project Scope to Promiscuous Enzymes Portion*

### Hypothesis:

> Any enzyme can be promiscuous. (Enzymes are differentially able to be promiscuous, especially with modern protein engineering techniques.) 

### Goal of model: 

> Predict an enzyme for a chemical transformation that doesn't have a known biocatalyst.

### Notes

* input target compound (substrate/product pair? that complicates things) - any route to this target is feasible

* RDKit substructure matching - figuring out if one chemical is part of another. *Constraint:* previous steps should be substructures. prevent edge case by only building, not breaking down things

* create tool for one-step transformations

* output: enzyme or list of enzymes, each with a score that we can rank based on how likely they are to have promiscuous activity that results in the creation of the input compound

* Focus: what type of enzymes? - pick an enzyme based on major substrate... narrow down enzymes that we are studying. pick less complex enzyme/substrate relationships

* EC numbers - choose a class and/or subclass to narrow scope. train model using these and other things as feature vectors. try with all of them and then limit the number of enzymes if it is messy.

### Question/Discussion:

What is our training set data? test set? 
> KEGG - query all enzymes with x > 1 rxn associated (cleaning this will be difficult), have list of enzyme/substrate/product/size of enzyme/extended info/MW/etc, group by common enzyme then characterize the shifts (looking at products) - 

how to get from one to the next? - RDKit to characterize the delta between the product compounds (tanimoto similarity index? substructure vs completely different? expected vs unexpected), training it on chemical similarity/relatvitiy, build list of tolerated shifts "plus methyl group, minus conjugation, etc", chemical constraints, another thing that RDKit can do is find the greatest common denominator/ max common substructure - chemical structure three parts: 1) rxn center (where chemistry occurs) 2) recognition part 3) variations - need some sort of algorithm that will assign the rxn center, can make a group using this information, characterize for each of promiscuous enzyme groups. training data looks like: promiscuous enzyme, rxn center, recognition part, variation, size, cofactor, etc etc. Then divide this pool into training and test set. train model to take one of the vectors and return an enzyme. test new substrate by input substrate, run the variation maker thing to create similar compounds, go to database and search enzymes that react on varied compounds, use model to score which of the shifts and the associated enzyme is most likely to be promiscuous.

*Did not select this idea:* Another potential approach: get substrate, apply similarity index, 
enzyme with original substrate -> expand (apply similarity index) to set of compounds -> divide (80/20) training and testing. training **Problem** we don't know which are known and which are hypothetical reactions

RDKit: compare substrate and product to find reaction center. 

Issue for data cleaning: how to remove reaction promiscuity

after the data cleaning and all that stuff: next step is grouping in Stephen's manner, the chemical shift?, if rxn center is easy to find we should, in one paper they limit the reaction by distance for promiscuity, 

maybe conserve bonds: within 3 bonds? within four bonds?




### Example

**How to use the tool:**

Input compound: phenol

1) define rxn center
2) vary structure outside of rxn center - get list of related compounds
3) take list of related compounds and search database for enzymes that make those compounds - 
4) get list of enzymes that have those varied compounds as product
5) ML to score enzymes for predicted promiscuity (how to build this?)

**How to build the tool:**

1) Access KEGG data
2) Select and vectorize features
3) ML
4) RDKit

**Constraints:**

- single step
- previous step is substructure 
- enzyme class
- substrate complexity
