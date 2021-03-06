# [RetroPath 2.0](http://www.jfaulon.com/retropath2-0-a-retrosynthesis-workflow-for-metabolic-engineers-biorxiv/)

This tool takes three inputs: source compounds (desired coumpound), reaction rules (should check RetroRules), and sink compounds (a repertoire of simpler starting materials)
By using their workflow, the desired pathway will be achieved. Their goal is to provide a pathway for expression in E. coli. I talked with their collaborators before, who do actual pathway implementation in E. coli, but didn't know they've gone this far.
There is a tool available for us to test but I cannot get it to work yet.
[See publication here](https://github.com/theicechol/metamoles/blob/master/Related%20articles/RetroPath_2.pdf)

*Ellie*:

I downloaded this and it looks like it is a pretty powerful tool. I have not succeeded in making it work, though, which means that it is not as user-friendly as it could be. Some things I immediately noticed:

- Requires 3-4 input csv files
- You need to have a set of reaction rules for it to follow, it doesn't know them itself
- The interface is very hard to use and completely unintuitive

# [RetroRules](https://retrorules.org/)

RetroRules is a database designed for pathway search (including enzyme promiscuity). The input can be either enzyme ID, reaction ID, chemical name, or InChI (similar to SMILES but contain more information).
[See publication here](https://github.com/theicechol/metamoles/blob/master/Related%20articles/RetroRules.pdf)

They have other bioinformatic tools available
* https://academic.oup.com/bioinformatics/article/34/12/2153/4841713
[See publication here](https://github.com/theicechol/metamoles/blob/master/Related%20articles/Selenzyme.pdf)