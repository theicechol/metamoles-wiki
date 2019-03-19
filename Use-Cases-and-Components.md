## Use Cases

**Basic**
- **Search for enzyme to create input molecule:** This use cases starts when a user inputs the PubChem ID of a molecule into the Metamoles package. This use case ends when a prediction about an enzyme that could produce the input molecule is made.
Components:
  - User input
    -ID
  - Enzyme data collection
    - KEGG promiscuous reactions info
    - SMILES of products, etc
  - Compound data collection
    - SMILES
  - Data generation for model
    - Comparison of products for each enzyme
  - Model generation
    - Train and test
  - Model output
    - Prediction
    - Quality of prediction
- **Retrieve information about model used for prediction:** This case starts when a user inputs the PubChem ID of a molecule. This use case ends when a prediction is made.
Components:
  - User input
    - ID
  - Enzyme data collection
    - KEGG promiscuous reactions info
    - SMILES of products, etc
  - Compound data collection
    - SMILES
    - Data generation for model
    - Comparison of products for each enzyme
  - Model generation
    - Train and test
  - Model output
    - Prediction
    - Quality of prediction

- **Train the regression/ML prior to deployment:** This use case begins when a developer inputs the PubChem ID of a molecule. This use case ends when the model has accessed all the training data.
Components:
  - Enzyme data collection
  - Compound data collection
  - Data generation for model
    - Comparisons
  - Regression/ML selection
  - Train the model with generated data
- **Test the regression/ML:** This use case starts when a developer uses known information to test the reliability of the model. This case ends when the model meets a level of accuracy that is appropriate for deployment.
Components:
  - Trained model
  - Withheld data

**Advanced**
- Real time search (calculate when called) versus recent update search (some data on hand)?
- Explore enzyme promiscuity (look at what’s happening in the background)
- Report experimental outcomes (positive and negative if people use our prediction)
- Offer different ML models or prediction methods (edited) 
- Included non-promismuous enzyme in the reaction search (or some non-enzymatic pathway)