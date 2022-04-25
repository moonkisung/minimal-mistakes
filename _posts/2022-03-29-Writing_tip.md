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

# Preserving Semtantics
- To incorporate the domain knowledge into pre-training more explicitly, MoCL [Sun et al., 2021] proposed a new augmentation operator called substructure substitution, in which a valid substructure in a molecule is replaced by a bioisostere [Meanwell, 2011] which produces a new molecule with similar physical or chemical properties as the original one.

- Also, they leave a future work to take the structural similarities between two graphs as supervision. Inspired by this, MoCL [Sun et al., 2021] first calculates the Tanimoto coefficient [Bajusz et al., 2015] between of two molecules as the measure of structural similarity, which serves as the supervisions for the pre-training.

- Initially, GraphCL [You et al., 2020] augments molecular graph data in the form of naive random corruption (e.g., dropping bonds, dropping atoms and etc.). However, these augmentations may alter molecular graph semantics completely even if the perturbation is weak. For example, dropping a carbon atom in the phenyl ring will alter the aromatic system and result in an alkene chain, which will drastically change the molecular properties. Besides, MoCL [Sun et al., 2021] attempts to incorporate domain knowledge into graph data augmentation via replacing valid substructures in molecular graph with bioisosteres that share similar properties. However, bioisosteres are used to modify some molecular properties as expected (e.g, reduce toxicity) in drug design [Mannhold et al., 2012], which may introduce incorrect supervision for molecular properties prediction such as toxicity prediction. We compare MolAug with these augmentations in section 4.5.

- In this section, we substitute MolAug with general graph augmentations including nodes drop(ND),edges perturbation(EP)in GraphCL[Youetal., 2020]and domain knowledge-enriched molecular graph augmentations(DK) in MoCL

- MoCL[40] proposes to replace valid substructures in molecular graph with bioisosteres that share similar properties. However, it requires expensive domain knowledge as guidance and cannot be applied in other domains like social graphs.

- The augmentation or perturbation of MoCL and our SimGRACE can preserve the class identity semantics well while GraphCL cannot.

- More recently, MoCL [40] proposes to incorporate domain knowledge into molecular graph augmentations in order to preserve the semantics. However, the domain knowledge is extremely expensive. Worse still, MoCL can only work on molecular graph data, which significantly limits their generality.


# 성과가 좋음
- Despite the fruitful progress, they still require tedious manual trial-and-errors, cumbersome search or expensive domain knowledge for augmentation selection. Instead, our SimGRACE breaks through state-of-the-arts GCL framework that takes semantic-preserved data augmentations as prerequisite.

# 풍부한 표현 학습
- The global-level knowledge encodes the similarity information between graphs in the entire dataset and helps to learn representations with richer semantics.