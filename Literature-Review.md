We can add our [annotated bibliographies](https://guides.library.cornell.edu/annotatedbibliography) here

### Yeon
**Coley, C. W., Rogers, L., Green, W. H., & Jensen, K. F. Computer-Assisted Retrosynthesis Based on Molecular Similarity. *ACS central science* (2017), 3(12), 1237-1245.**
> The authors used molecular similarity to rank one-step retrosynthetic disconnections based on analogy to precedent reactions. Reaction templates were used only at the most rudimentary level to generate chemically valid precursor molecules. Similarity was calculated by reflecting the extent of overlapping substructures. Quantification of molecular similarity generally requires fingerprinting technique and this research focus their evaluation on Morgan circular fingerprint as implemented in RDKit. 


See further explanation in the [full review](https://pubs.acs.org/doi/full/10.1021/acscentsci.7b00355)

### Ice
**Granda, J. M., Donina, L., Dragone, V., Long, D.-L., Cronin, L. Controlling an organic synthesis robot with machine learning to search for new reactivity. *Nature* (2018), 559, 378-381.**
> The authors utilized supported vector machine (SVM) to predict the reactivity of chemical reactions. The model was trained on randomly generated chemical reactions which were performed by a robot equipped with sufficient characterization instruments. The generated model can efficiently predict the reactivity the other reactions with the reaction universe. The SVM model might be applicable to this project using similar vector representation shown in the article.

See further explanation in the [full review](https://www.nature.com/articles/s41586-018-0307-8)

### Ellie
**Swainston N, Batista-Navarro R, Carbonell P, Dobson PD, Dunstan M, Jervis AJ, et al. (2017) biochem4j: Integrated and extensible
biochemical knowledge through graph databases. *PLoS ONE* 12(7): e0179130.**
> The authors created a graph database (biochem4j) that integrates organism, enzyme, reaction, and product data from ChEBI, MNXref, Rhea, KEGG, UniProt, and NCBI. The data exists as nodes that are connected by specified relationships; querying occurs using the CYPHER language. This database was created with metabolic engineering in mind, so it readily connects chemical products with pathways from a starting material. The [text scraping](https://github.com/synbiochem/biochem4j) and some implementation code is in Python and has [Python dependencies](https://github.com/synbiochem/synbiochem-py).

See further explanation in the [full review](https://doi.org/10.1371/journal.pone.0179130)

### Ellie
**Jeffryes et al. MINEs: open access databases of computationally predicted enzyme promiscuity products for untargeted metabolomics. *J Cheminform* (2015) 7:44.**
> The authors created MINEs as an extension to databases with known enzyme products and metabolites. The [database](http://minedatabase.mcsanl.gov) was populated using the Biochemical Network Integrated Computational Explorer algorithm to propose novel chemical structures and reactions for the database. These novel entries are suspected enzyme side reactions that account for the currently unidentified peaks in metabolomics (mostly LCMS) data.

*Could be useful in terms of predicted enzyme promiscuity*

See further explanation in the [full review](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-015-0087-1)

### Ellie
**Seglers, M.H.S. and Mark. P. Waller. Neural-Symbolic Machine Learning for Retrosynthesis and Reaction Prediction. *Chem. Eur. J.* (2017), 23, 5966-5971.** 
> The authors developed a neural-symoblic model capabale of reaction prediction and retrosynthesis. The model was trained with known reactions and the corresponding reaction rule with the goal of learning functional group patterns and how they changed during reactions. Molecules were encoded as Extended-Connectivity Fingerprints (ECFP4), creating vectors that contain a count of occuring functional groups. 

*Six hours to train on an **impressive** GPU - we will need to limit our scope to things we can do in a similar timeframe with our computing resources*

*Everything I've read so far uses RDKit*

See further explanation in the [full review](https://onlinelibrary.wiley.com/doi/full/10.1002/chem.201605499) or [supporting information](chem201605499-sup-0001-misc_information.pdf)

### Phil
**Pertussi, D., Moura, M., Jeffryes, J., Prabhu, S., Walters Biggs, B., Tyo, K.E. Predicting novel substrates for enzymes with minimal experimental effort with active learning. *Metabolic Engineering* (2017), 44, 171-181.**
> The authors developed an [algorithm (SimAL)](https://github.com/tyo-nu/SimAL) that utilizes cheminformatics in a support vector machine learning approach to predict an enzyme's promiscuity with 33% less experimental observations. The intended purpose of this characterization of promiscuity is to determine the most informative substrates to test next for a given enzyme.

*This is a helpful paper because we want to do essentially the same thing but in reverse, choosing enzymes that are potentially promiscuous towards our selected substrate.*

See further explanation in the [full review](https://www.sciencedirect.com/science/article/pii/S1096717617300708)

### Yeon
**Feng, Fan, Luhua Lai, and Jianfeng Pei. "Computational chemical synthesis analysis and pathway design." Frontiers in chemistry 6 (2018).**
> The authors introduce two-step models which combine reaction rules and statistical method. Machine learning plays the role of decision making and the decision gets generated using reaction rules or structural rules. They also mention about fully end-to-end retrosynthesis analysis with deep neural networks. However, they point out the low accuracy of retrosynthesis prediction of this method. 
[Link to publication](https://www.frontiersin.org/articles/10.3389/fchem.2018.00199/full)


### Stephen
**Hadadi, Noushin, et al. "ATLAS of biochemistry: a repository of all possible biochemical reactions for synthetic biology and metabolic engineering studies." ACS synthetic biology 5.10 (2016).**
> The authors built an online database they are calling the “ATLAS of biochemistry” that uses BNICE (Biochemical Network Integrated Computational Explorer) framework to connect KEGG metabolites to one another via predicted enzymatic reactions. The database successfully reconstructed 6651 out of 9911 annotated KEGG reactions (as of 2015), and suggested over 130,000 hypothetical reactions between metabolites, for which enzymes have yet to be discovered.

_One possible project scope refinement direction we could take: looking at the predicted enzyme reactions and attempting to predict candidate genes to investigate, or at least candidate genomes in which the enzyme might reside._

Full paper can be found [here](https://pubs.acs.org/doi/abs/10.1021/acssynbio.6b00054) and you can see the database homepage [here](http://lcsb-databases.epfl.ch/atlas/Home)

### Yeon
**Heckmann, David, et al. "Machine learning applied to enzyme turnover numbers reveals protein structural correlates and improves metabolic models." Nature communications 9.1 (2018): 5252.**

> Authors used machine learning to predict catalytic turnover numbers in E-coli based on integrated at a on enzyme biochemistry, protein structure, and network context. They combined known correlates of cat with novel features for enzyme structure, biochemical mechanism, network context, and assay condition to build machine learning models of k cat in vitro and k appmax. Although this method gives more insight to mechanistic metabolic models, one major limitation of statistical modelling of catalytic turnover numbers is the small size of the dataset (k cat in vitro and k app, max). The most promising output k app, max is limited to unique homomers. 
See publication [here](https://www.nature.com/articles/s41467-018-07652-6)

### Stephen
**Wang, Lin, et al. "A review of computational tools for design and reconstruction of metabolic pathways." Synthetic and systems biotechnology 2.4 (2017)**

> In this paper the authors review a broad range of existing computational tools for retrobiosynthetic pathway design. They group these tools into three categories based on network representation, and search strategy: graph-based, stoichiometry-based, and retrosynthesis-based. The authors go into some technical detail around key requirements of a design tool, including the database, network representation, network pruning, search algorithm, and pathway ranking. For each of these requirements the authors discuss different existing implementation strategies and tradeoffs between one implementation over the other. It looks as though a majority of the tools reviewed use KEGG as their database.

Full paper [here](https://www.sciencedirect.com/science/article/pii/S2405805X17300820) and some helpful graphics [here](https://github.com/theicechol/metamoles/wiki/Review-of-metabolic-pathway-design-tools-(2017))
In the computational tools review, it concludes "Overall, a completely automated pipeline that goes from selection of source and target molecule to the final output of DNA sequences of a pathway would significantly facilitate the discovery of new metabolic pathways for various applications." This might be something we could build.

### Ice
Segler, M. H. S., Preuss, M., Waller, M. P. "Planning chemical synthesis with deep neural networks and symbolic AI" **2018**, _Nature_ 555, 604–610
> The author made a platform for reaction planning based on retrosynthesis. They used MTCS (Monte-Carlo Tree Search) and Neural Networks to build to the platform. The data used for training came from Reaxys database in which they extract reaction center from the published chemical reactions prior to 2015 for training and the rest for testing. The double-blind test with chemistry graduate students suggested that this search is not significantly inferior to those published in the literature.

[See details here](https://www.nature.com/articles/nature25978)

Lee, S. Y., et. al. "A comprehensive metabolic map for production of bio-based chemicals" **2019**, _Nature Catalysis_, 2, 18-33.
> This review provides resourceful chemical synthesis pathway from both biological and chemical syntheses. General compounds for industrial usage are listed and mapped. A cross-linked pathway with biological/chemical reactions are provided as well. This should be a good start to look for a specific pathway for testing.

See original review [here](https://www.nature.com/articles/s41929-018-0212-4)

de Souza, R. O. M. A., Miranda, L. S. M., Bornscheuer, U. T. "A Retrosynthesis Approach for Biocatalysis in Organic Synthesis" **2017**, _Chem. Euro. J._, 23, 12040-12063.
> This review provided an easy explanation of biochemical retrosynthesis by introducing a biocatalytic pathway for chemical transformation of each synthon (fragment) with side-by-side comparison in organic synthesis. See the summary part for short intuition. If this bio-retrosynthesis style can be made into a software tool, that's our project.

See original review [here](https://onlinelibrary.wiley.com/doi/full/10.1002/chem.201702235)