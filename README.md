# BBB permeability prediction with Deep Learning

In my FinalDegreeProject, I trained a deep neural network model to predict permeability across the blood-brain barrier (BBB), a key challenge in central nervous system drug development.

The model was trained using the **B3DB dataset**, a curated and diverse molecular database specifically designed for BBB permeability studies. This dataset was published by Meng et al. (2021):

> Meng, F., Xi, Y., Huang, J., & Ayers, P. W. (2021). A curated diverse molecular database of blood-brain barrier permeability with chemical descriptors. *Scientific Data*, 8(1), 289.  
> [https://doi.org/10.1038/s41597-021-01069-5](https://doi.org/10.1038/s41597-021-01069-5)

The B3DB dataset includes two subsets based on data type: **classification** and **regression**.  
- The **classification dataset** contains binary labels (`BBB+` and `BBB−`) indicating whether a compound can cross the blood-brain barrier.  
- The **regression dataset** contains continuous values representing `logBB` (logarithm of the brain-to-blood concentration ratio), a quantitative measure of permeability.

Each entry in the dataset includes a SMILES string (Simplified Molecular Input Line Entry System), which encodes the molecular structure. These SMILES were used to generate:
- **Molecular descriptors** (numerical representations of chemical and physical properties).
- **Morgan fingerprints** (binary vectors encoding substructural features of molecules).

Both types of features were used as inputs for model training and evaluation.

I implemented data preprocessing, feature generation, model development, and evaluation using Python libraries such as **pandas**, **RDKit**, **TensorFlow/Keras**, and **scikit-learn**.

**Main objectives of the project**:
- Develop predictive models for BBB permeability using molecular descriptors and fingerprints.
- Evaluate model performance using metrics such as accuracy, F1 score, ROC-AUC, and precision-recall.
- Explore feature importance and assess model interpretability.

**Future work**:
- Integrating graph neural networks (GNNs) to directly learn from molecular graph structures.
- Applying transfer learning techniques using pre-trained models in cheminformatics and molecular property prediction.
