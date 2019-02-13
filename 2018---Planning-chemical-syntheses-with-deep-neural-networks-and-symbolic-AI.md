# Planning chemical synthesis with deep neural networks and symbolic AI
## (Link to the original paper)[https://www.nature.com/articles/nature25978]
From Mark P. Waller group

### Summary
The authors aimed to build a platform for chemical reaction design using deep learning to achieve the level that chemists can do. In this work, they used a Monte-Carlo tree search and symbolic AI. Start by breaking down the compound into different synthons (parts) and repeat that to the simple fragments (Not sure the criteria for simple). The process consists of three neural networks (MTCS) which do selection, expansion, and rollout. These neural networks are for ranking the best tree found. The best tree from MCTS was claimed to be comparable to a graduate student from the double-blind test. I'm skeptical on this though.