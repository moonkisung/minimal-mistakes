---
layout: single
title: "논문에서 쓰기 좋은 표현"
---

# Comprehensive = Extensive
# 3D information
- 3D information = 3D coordinates = 3D coordinate information = 3D positional information = 3D position = spatial position = spatial information = 3D spatial information = 3D structural information

# Regression Dataset 이유
- Since the tasks of the regression datasets, such as the water solubility prediction in the ESOL dataset and the electronic properties prediction in the QM7 dataset, are much more correlated to the molecular geometries than the classification tasks, ChemRL-GEM achieves more considerable improvement on the regression datasets compared to the classification datasets.
- physical chemistry datasets (ESOL, Freesolv)
- quantum-mechanical (QM) properties, that are strongly tied to a low energy 3D structure (also referred to as
conformer), has been less explored.
- physical chemistry and quantum mechanics are more related to molecular geometries compared to those of biophysics and physiology.

# Scaffold splitting
- There are several popular splitting methods used in molecular property prediction datasets, including
random splitting, scaffold splitting [2] and random scaffold splitting. Scaffold splitting and random
scaffold splitting offer more challenging yet realistic ways of splitting by keeping the molecules with
the same scaffold in either the train, validation, or the test set.

- Following the previous work [23], we split all the 12 datasets with scaffold split [37], which splits
molecules according to the their scaffold (molecular substructure). Rather than splitting the dataset
randomly, scaffold split is a more challenging splitting method, which can better evaluate the
generalization ability of the models on out-of-distribution data samples. Based on scaffold split, we
split the molecules in each dataset into training set, validation set, and test set by the ratio of 8:1:1.

- Scaffold splitting splits the molecules with distinct two-dimensional structural frameworks into different subsets. It is a more challenging but practical setting since the test molecular can be structurally different from the training set. Here we apply these splitting methods to construct the train/validation/test sets.

- For all datasets except QM9, we use the scaffold split to create an 80/10/10 train/valid/test split as suggested in45. Unlike the common random split, the scaffold split, which is based on molecular substructures, makes the prediction task more challenging yet realistic. QM9 follows the random splitting setting as implementations of most related works19, 44, 52 for comparison.

- Scaffold splitting splits the samples based on their two-dimensional structural frameworks,45 as implemented in RDKit.46 Since scaffold splitting attempts to separate structurally molecules in the training/validation/test
sets, the scaffold split offers a greater challenge for learning algorithms than the random split.

- Scaffold split은 molecular data를 their substructure에 따라 나누기 때문에 train/val/test set이 구조적으로 다르게 구성된다. 따라서 일반적인 split 방법보다 prediction이 challenge 하고 모델의 일반화 능력이 요구되기 때문에 molecular dataset에 널리 쓰이고 있다.



- Despite the fruitful progress, they still require tedious manual trial-and-errors, cumbersome search or expensive domain knowledge for augmentation selection. Instead, our SimGRACE breaks through state-of-the-arts GCL framework that takes semantic-preserved data augmentations as prerequisite.