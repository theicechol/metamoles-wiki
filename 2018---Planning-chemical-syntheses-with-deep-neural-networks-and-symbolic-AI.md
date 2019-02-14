# Planning chemical synthesis with deep neural networks and symbolic AI
## [Link to the original paper](https://github.com/theicechol/metamoles/blob/master/Related%20articles/Planning_chemical_syntheses_with_deep_neural_networks_and_sympolic_AI.pdf)
From Mark P. Waller group

### Summary
The authors aimed to build a platform for chemical reaction design using deep learning to achieve the level that chemists can do. In this work, they used a Monte-Carlo tree search and symbolic AI. Start by breaking down the compound into different synthons (parts) and repeat that to the simple fragments (Not sure the criteria for simple). The process consists of three neural networks (MTCS) which do selection, expansion, and rollout (3N-MTCS). These neural networks are for ranking the best tree found. The best tree from MCTS was claimed to be comparable to a graduate student from the double-blind test. I'm skeptical on this though.

### Data Science Methodology
The previous work mentioned in this work use heuristic best first search (BFS) that they claimed they could overcome.
12.4 million single-step reactions from ***Reaxys*** by selecting reactions published before 2015 for training and after 2015 for testing. In their extraction, they extract only **reaction center** elements (I think it is the bond-making and bond-breaking parts). 

### low efficiency reaction prediction
Since bad reactions or failed reactions are rarely reported, they assume hypothetical products for the reaction that was not reported in a high yield reaction to be a low-efficiency path.

### Integration of MTCS and neural networks
1) Selection: make a retrosynthesis tree
2) Expansion: iterations for the following
3) Rollout: make a ranking of each tree
4) Update: update the finding

### Double-blind tests
Give two choices from MCTS and literature and let the graduate students choose which one is preferred. The MCTS generated scheme is not significantly inferior which is better than BFS that is significantly inferior.

### Adaptations to our project
The MTCS and neural networks processes might be compatible with our project. The data retrieving tool would be of use as well.