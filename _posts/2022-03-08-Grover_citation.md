---
layout: single
title: "GROVER 인용 논문 정리"
---
# 피인용수
- GROVER (NeurIPS 2020)
- we apply three independent runs on three random seeded scaffold splitting and report the mean and standard deviations.
- cited by 101

<br />

# 참고 조건
1. 20년 이후 논문
2. ESOL, Freesolv, QM7, QM8 중 2개 이상 결과 제시
3. 실험 조건 확인할 것 (3 Scaffold, 8:1:1)
4. published 된 논문

<br />

# 인용 논문
## 1. Geometry-enhanced molecular representation learning for property prediction
  - Nature Machine Intelligence, 2022
  - Following the previous work, we split all the datasets with scaffold split. We execute four independent runs for each method and report the mean and the standard deviation of the metrics.
  - ESOL, Freesolv, QM7, QM8
  - cited by 1
  - 인용 가능
    
## 2-1. An effective self-supervised framework for learning expressive molecular global representations to drug discovery
  - Briefings in Bioinformatics 2021, MPG
  - We followed the same experimental setting as GROVER[46]. Each dataset was split into train/validation/testset by the random scaffold split with a ratio of 8:1:1
  - ESOL, freesolv
  - SOTA
  - cited by 9
  - 인용 가능하지만 SOTA..

## 2-2. Learn molecular representations from large-scale unlabeled molecules for drug discovery
  - arxiv 2020, MPG
  - SOTA
  - cited by 10


## 3. Learning Attributed Graph Representations with Communicative Message Passing Transformer
  - IJCAI 2021
  - We used a 5-fold cross validation with scaffold split and replicated experiments on each tasks for five times.
  - ESOL, Freesolv
  - 인용 가능
  - cited by 7
  

## 4. MolCLR

<br />

# 참고 논문
1. Pre-training Molecular Graph Representation with 3D Geometry
   - ICLR 2022
   - For each downstream task, we report the mean (and standard variance) RMSE of 3 seeds with scaffold splitting.
   - ESOL
   - 4.2 Baselines 검색
   - https://openreview.net/forum?id=xQUe1pOKPam 참고
   - 인용 불가능 (dataset 부족)
   - 내용은 참고

2. Pre-training Molecular Graph Representation with 3D Geometry– Rethinking Self-Supervised Learning on Structured Data
   - 2021 GraphMVP
   - top machine learning conferences 검색

3. PRE-TRAINING MOLECULAR GRAPH REPRESENTATION WITH 3D GEOMETRY
    - 2021 Technical Report, GraphMVP

4. Multilingual Molecular Representation Learning via Contrastive Pre-training
   - ACL 2022 
   - ESOL, freesolv but random splitting
   - 인용 불가능 (세팅 다름)

5. 3D Infomax improves GNNs for Molecular Property Prediction
    - NeurIPS 2021 (Poster)

6. Improving Molecular Contrastive Learning via Faulty Negative Mitigation and Decomposed Fragment Contrast
   - arxiv 2022
   - During fine-tuning, each dataset is split into train/validation/test sets through scaffold split by the ratio of 80/10/10 following previous molecule SSL works.
   - ESOL, Freesolv, QM7, QM8
   - cited by 0
   - abstract 및 baseline 참고할만 함(CL 끼리만 비교하여 SOTA)
   - 인용 애매 (성능은 우리것 보다 낮지만 아직 accept X)

7. Do Large Scale Molecular Language Representations Capture Important Structural Information?
   - arxiv 2021, MOLFORMER-XL
   - freesolv, QM7, QM8 사용하지만 setting 다름
   - cited by 1

8.  STEPPING BACK TO SMILES TRANSFORMERS FOR FAST MOLECULAR REPRESENTATION INFERENCE
   - arxiv 2022
   - freesolv, QM7, QM8 사용하지만 setting 다름
   - 인용 불가 (data는 OK지만 setting 다름)
   - cited by 0

9. Learn molecular representations from large-scale unlabeled molecules for drug discovery
    - arxiv 2020, MPG
    - SOTA
    - cited by 10

11. Motif-based Graph Self-Supervised Learning for Molecular Property Prediction
   - NeurIPS 2021
   - 4.1 Experimental Settings
   - cited by 6
   - 인용 불가 (데이터셋 사용X)

12. Dual-view Molecule Pre-training
   - arxiv 2021
   - On the other hand, to compare with [45, 32], we follow their ways to split the data and conduct another group of experiments. Specifically, we use scaffold splitter to generate the training (80%), validation (10%) and test (10%) sets with 3 different seeds.
   - ESOL, QM7, QM8
   - parameter, time도 비교
   - SOTA
   - 인용하기 애매 (우리보다 좋음)

13. Towards Effective and Generalizable Fine-tuning for Pre-trained Molecular Graph Models
   - biorxiv 2022
   - 인용 불가 (너무 최신)

14. Deep Molecular Representation Learning via Fusing Physical and Chemical Information
    - NeurIPS 2021
    - ESOL, freesolv, QM7, QM8
    - 인용 불가 (세팅 다름)

15. 3D-TRANSFORMER: MOLECULAR REPRESENTATION WITH TRANSFORMER IN 3D SPACE
    - arxiv 2021
    - QM7, QM8
    - cited by 2
    - 인용 애매 (not accepted)

16. Graph Self-supervised Learning with Accurate Discrepancy Learning
   - 4.1의 **Models** 살펴볼 것

17. Molecular Contrastive Learning with Chemical Element Knowledge Graph
   - AAAI 2022
   - ESOL, freesolv but random splitting
   - 참고하기 좋음
   - 인용 불가 (SOTA지만 세팅 다름)

18. MolCloze: A Unified Cloze-style Self-supervised Molecular Structure Learning Model for Chemical Property Prediction
    - BIBM 2021
    - 인용 불가 (데이터셋 사용X)
    - 
19. Molecular Graph Contrastive Learning with Parameterized Explainable Augmentations
    - BIBM 2021
    - 인용 불가 (데이터셋 사용X)

20. Comparison of Atom Representations in Graph Neural Networks for Molecular Property Prediction
    - Prediction 잘하거나 못하는 Molecule 시각화
    - Fig 4 참고

21. Bringing Your Own View: Graph Contrastive Learning without Prefabricated Data Augmentations
    - arxiv 2022
    - cited by 0
23. Cross-dependent graph neural networks for molecular property prediction
    - Bioinformatics, 2022
    - cited by 0
<br />

# 참고 리뷰 논문
1. Review of unsupervised pretraining strategies for molecules representation
   - pretext task에 대한 정리가 잘 되어 있음

<br />