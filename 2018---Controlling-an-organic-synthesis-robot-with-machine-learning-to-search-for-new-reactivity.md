# Controlling an organic synthesis robot with machine learning to search for new reactivity
## [Link to the original paper](https://github.com/theicechol/metamoles/blob/master/Related%20articles/Controlling_an_organic_synthesis_robot_with_machine_learning_to_search_for_new_reactivity.pdf)

A paper from U of Glasgow, UK

### Summary
In brief, the author manufactured a chemical synthesis robot equipped with spectroscopic instruments (NMR, FTIR, and MS) which are sufficient for characterization. The reactions were monitored real-time. Per observation, the faster kinetics means higher reactivity. Then, the randomly generated chemical reactions were performed by the robot and the acquired data were utilized for machine learning model. Finally, the model can be used to predict the reactivity of the input reaction.

### Data Science Methodology
This work use SVM (supported vector machine) for the machine learning method. The created model is called LDA (linear discriminant analysis) which was trained with collected data which can be used to predict the reactivity of a particular reaction. There is a term one-hot encoding which I don't yet understand what it is. Tanimoto similarity index was mentioned as well for the determination of the molecules' similarity

### Application to our ideas
The compounds in chemical reactions were categorized into reactant1, reactant2, ligand, base, and solvent. This annotation of the molecules may be applied to a biochemical reaction by replacing ligand to cofactors, e.g., Mg<sup>2+</sup>, PLP, and alter base into ATP, NADPH or the compounds with a similar role. The solvent in a biochemical reaction should be neglected even though culture media can affect the production of the enzyme but let's leave it for now.
The other parameters are reaction temperature and time. These two parameters are relevant to our work as well. The kinetic parameter might be of use for evaluation of reaction efficiency. Biochemical reaction temperature has a narrower range since we usually perform metabolic engineering for cell culture from 25 to 37 °C.

### Additional notes
The impact of this paper came from the discovery of new reactions which, in my opinion, beyond chemists' intuition and eagerness. Let's say; chemists are less likely to try those reactions because they are too abnormal. Additionally, per my understanding, the reaction set-up in this paper may use 1:1:1 stoichiometric ratio which is not true in the catalytic reaction. I haven't dig deeper in SI yet, but the providing characterization data is not the level provided in general organic chemistry journal.
This approach can be applied to available published datasets as well but was not fully explained in the manuscript.