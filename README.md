# Learning binding avidity landscapes of T-cell receptors

A diverse repertoire of surface receptors on T-cells allows the adaptive immune system to detect a wide range of pathogens and initiate an immune response. The ability of these receptors to bind self or pathogenic epitopes is heavily influenced by the CDR3 region residing within the $\beta$ chain of the receptor. Identifying common patterns in these sequences may therefore give insight into the challenge of predicting epitope specificity. In this project, we infer an independent-site Potts model to describe sequences specific to the YLQPRTFLL and GILGFVTLL epitopes. Furthermore, we investigated the impacts of clustering these sequences to establish multiple localised models, alongside fine-tuning pseudocounts to enhance prediction accuracy.

- `CDR3B Sequences (Preprocessing).ipynb` preprocesses CDR3B sequences sourced from the VDJdb database [1], and Tanno *et al*. [2] by removing redundancies.
- `Functions.ipynb` contains most of the relevant functions
- `Alignment and clustering.ipynb` pads and clusters the sequences at various thresholds
- `Probability Matrices.ipynb` calculates and stores the probability matrices for each cluster
- `Threshold.ipynb` explores the effect of changing the clustering cutoff distance $t$ on classifier accuracy
- `Pseudocount.ipynb` explores the effect of changing the frequency pseudocount $\theta$ on classifier accuracy
- `K-Nearest Neighbours.ipynb` uses a KNN classifier to predict the epitope specificity at various $k$.


### References 

[1] M. Goncharov, D. Bagaev, D. Shcherbinin, I. Zvyagin, D. Bolotin, P. G. Thomas, A. A. Minervina, M. V. Pogorelyy, K. Ladell, J. E. McLaren, *et al*., “VDJdb in the Pandemic Era: a Compendium of T Cell Receptors Specific for SARS-CoV-2,” Nature Methods, vol. 19, no. 9, pp. 1017–1019, 2022.

[2] H. Tanno, T. M. Gould, J. R. McDaniel, W. Cao, Y. Tanno, R. E. Durrett, D. Park,
S. J. Cate, W. H. Hildebrand, C. L. Dekker, *et al*., “Determinants governing T Cell
Receptor $\alpha$/$\beta$-chain pairing in repertoire formation of identical twins,” Proceedings
of the National Academy of Sciences, vol. 117, no. 1, pp. 532–540, 2020.

