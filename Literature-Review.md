We can add our [annotated bibliographies](https://guides.library.cornell.edu/annotatedbibliography) here

**Coley, C. W., Rogers, L., Green, W. H., & Jensen, K. F. Computer-Assisted Retrosynthesis Based on Molecular Similarity. *ACS central science* (2017), 3(12), 1237-1245.**
> The authors used molecular similarity to rank one-step retrosynthetic disconnections based on analogy to precedent reactions.

See further explanation in the [full review](https://github.com/theicechol/metamoles/Related-articles/Computer-Assisted%20Retrosynthesis%20Based%20on%20Molecular%20Similarity.pdf)

**Granda, J. M., Donina, L., Dragone, V., Long, D.-L., Cronin, L. Controlling an organic synthesis robot with machine learning to search for new reactivity. *Nature* (2018), 559, 378-381.**
> The authors utilized supported vector machine (SVM) to predict the reactivity of chemical reactions. The model was trained on randomly generated chemical reactions which were performed by a robot equipped with sufficient characterization instruments. The generated model can efficiently predict the reactivity the other reactions with the reaction universe. The SVM model might be applicable to this project using similar vector representation shown in the article.

See further explanation in the [full review](https://github.com/theicechol/metamoles/wiki/2018---Controlling-an-organic-synthesis-robot-with-machine-learning-to-search-for-new-reactivity)

**Swainston N, Batista-Navarro R, Carbonell P, Dobson PD, Dunstan M, Jervis AJ, et al. (2017) biochem4j: Integrated and extensible
biochemical knowledge through graph databases. *PLoS ONE* 12(7): e0179130.**
> The authors created a graph database (biochem4j) that integrates organism, enzyme, reaction, and product data from ChEBI, MNXref, Rhea, KEGG, UniProt, and NCBI. The data exists as nodes that are connected by specified relationships; querying occurs using the CYPHER language. This database was created with metabolic engineering in mind, so it readily connects chemical products with pathways from a starting material. The [text scraping](https://github.com/synbiochem/biochem4j) and some implementation code is in Python and has [Python dependencies](https://github.com/synbiochem/synbiochem-py).

See further explanation in the [full review](https://doi.org/10.1371/journal.pone.0179130)

**Jeffryes et al. MINEs: open access databases of computationally predicted enzyme promiscuity products for untargeted metabolomics. *J Cheminform* (2015) 7:44.**
> The authors created MINEs as an extension to databases with known enzyme products and metabolites. The [database](http://minedatabase.mcsanl.gov) was populated using the Biochemical Network Integrated Computational Explorer algorithm to propose novel chemical structures and reactions for the database. These novel entries are suspected enzyme side reactions that account for the currently unidentified peaks in metabolomics (mostly LCMS) data.

*Could be useful in terms of predicted enzyme promiscuity*

See further explanation in the [full review](https://github.com/theicechol/metamoles/blob/master/Related%20articles/MINEsOpenAccessDatabasesOfComp.pdf)

**Seglers, M.H.S. and Mark. P. Waller. Neural-Symbolic Machine Learning for Retrosynthesis and Reaction Prediction. *Chem. Eur. J.* (2017), 23, 5966-5971.** 
> The authors developed a neural-symoblic model capabale of reaction prediction and retrosynthesis. The model was trained with known reactions and the corresponding reaction rule with the goal of learning functional group patterns and how they changed during reactions. Molecules were encoded as Extended-Connectivity Fingerprints (ECFP4), creating vectors that contain a count of occuring functional groups. 

*Six hours to train on an **impressive** GPU - we will need to limit our scope to things we can do in a similar timeframe with our computing resources*

*Everything I've read so far uses RDKit*

See further explanation in the [full review](https://github.com/theicechol/metamoles/blob/master/Related%20articles/Neural-Symbolic%20Machine%20Learning%20for%20Retrosynthesis.pdf) or [supporting information](chem201605499-sup-0001-misc_information.pdf)

**Pertussi, D., Moura, M., Jeffryes, J., Prabhu, S., Walters Biggs, B., Tyo, K.E. Predicting novel substrates for enzymes with minimal experimental effort with active learning. *Metabolic Engineering* (2017), 44, 171-181.**
> The authors developed an [algorithm (SimAL)](https://github.com/tyo-nu/SimAL) that utilizes cheminformatics in a support vector machine learning approach to predict an enzyme's promiscuity with 33% less experimental observations. The intended purpose of this characterization of promiscuity is to determine the most informative substrates to test next for a given enzyme.

*This is a helpful paper because we want to do essentially the same thing but in reverse, choosing enzymes that are potentially promiscuous towards our selected substrate.*

See further explanation in the [full review]
()