# hlink: historical record linkage

A working paper on the creation and applications of this program can be found at <https://www.tandfonline.com/doi/full/10.1080/01615440.2021.1985027>. A publication on the same topic is forthcoming.

## Docs

Documentation site can be found [here](https://pages.github.umn.edu/mpc/hlink).    
This includes information about installation and setting up your configuration files.

An example script and config file can be found in the `examples` directory.

## Overview

Hlink is designed to link two datasets. The primary use case was for linking demographics in the Household -> Person hierarchical structure, however it can be used to link generic datasets as well by skipping the Household linking task. It allows for probabilistic and deterministic record linkage, and provides functionality for the following tasks:

1. Preprocessing: preprocess each dataset to clean and or transform it in preparation for linking.
2. Training: train ML models on a set of features and compare results between models.
3. Matching: match two datasets using a model created in training or with deterministic rules.
4. Household linking: using the results from an individual linking process, compare household members of linked records to generate additional links.
5. Reporting: generate summarized information on linked datasets.
6. Model Exploration: compare various models and hyperparameter matrices to choose production model specs.

In addition, it also provides functionality for the following research/development tasks:
1. Model Exploration and Household Model Exploration: Use a matrix of models and hyper-parameters to evaluate model performance and select a model to be used in the production run.  Also generates reports of suspected false positives and false negatives in the specified training data set if appropriate config flag is set.
2. Reporting: Generate reports on the linked data.
