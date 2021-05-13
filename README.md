# Lipophilicity

This model has been developed using GROVER, a Graph Neural Network pretrained with 10 million unlabelled molecules from ChEMBL and ZINC15. GROVER has then been fine-tuned to predict Lipophilicity using the Lipo dataset curated by MoleculeNet. This dataset collects experimental results for octanol/water distribution coefficient from ChEMBL molecules.
GROVER predictions consistently outperformed other state-of-the-art methods for Lipo and other benchmark datasets from [MoleculeNet](https://pubs.rsc.org/en/content/articlelanding/2018/sc/c7sc02664a#!divAbstract).

## Summary
* Predicts **Lipophilicity** for small molecules.
* Takes **compound structures** as input.
* Trained with the benchmark **Lipo MoleculeNet** dataset (4200 molecules).
* Results validated **in-silico** against baseline methods for the same dataset.
* Published in [*Rong et al, Advances in Neural Information Processing Systems 2020*](https://papers.nips.cc/paper/2020/hash/94aef38441efa3380a3bed3faf1f9d5d-Abstract.html)
* Processed data can be found [here](https://github.com/tencent-ailab/grover)

## Specifications
* Input: SMILES string (also accepts an InChIKey string or a molecule name string, and converts them to SMILES)
* Endpoint: prediction of the ability of the compound to dissolve in fat (measured by its octanol/water distribution coefficient)
* Results interpretation: 0: lipophobic - 1: highly lipophilic

## History
1. Model was downloaded on 12.05.21 from [TencentAILab](https://github.com/tencent-ailab/grover).
2. We duplicated task/predict.py and scripts/save_features.py from Tencent GitHub repository.
3. Model was incorporated to Ersilia on 13/05/2021.
