# **Certifying Properties of Deep Networks by Taking them into Shallow Waters**

## Master Thesis Project - ETH Zurich / Imperial College London

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

Published in <strong>ETH Zürich</strong> Research Collection, 2020 - [Paper](https://www.research-collection.ethz.ch/handle/20.500.11850/531617)

Author: <strong>Konstantinos Barmpas</strong> | Advisors: Yannic Kilcher, Kevin Roth, David Haber | Supervisor: Thomas Hofmann 

[distillation]: ./images/distillation.png "Model Distillation"
[pruning]: ./images/pruning.png "Pruning"
[adversarial]: ./images/adversarial.png "Adversarial"
[certification]: ./images/certification.png "Certification"

**Abstract**

Over the last decades, complex deep neural networks have revolutionized Artiﬁcial Intelligence (AI) research. These models can now achieve impressive performances on various complex tasks like recognition, detection and image semantic segmentation, achieving accuracy close to, or even better, than human perception. However, these neural networks require to be both deep and complex and this complexity constitutes a danger for the safety veriﬁcation (certiﬁcation) and interpretability of a neural network model.

This project explores the certiﬁcation properties of complex neural networks by taking them into ”shallow waters”. First, a detailed investigation of efﬁcient model distillation techniques is conducted. Then, using the shallow models trained with these distillation methods, several of their properties are further explored, among them adversarial robustness and their performance under parameter reduction procedures. Finally, by combining network’s convex relaxation with model compression, the certiﬁcation area of shallow student models (derived from either normally or robustly trained teacher networks) is researched. Through all of these experimental results, it is empirically demonstrated and proved that model distillation leads to shallow models with larger certiﬁcation areas than their equivalent complex teacher networks. Therefore, based on this thesis evidence, shallow distillated networks constitute a possible solution to the safety and interpretability issues that modern complex Artiﬁcial Intelligence (AI) models face.

**Information**

Master Thesis Project at the [[Data Analytics Lab](http://www.da.inf.ethz.ch/)] in collaboration with [[Daedalean AI](https://daedalean.ai/)]. 

Supervised by [[Professor Dr. Thomas Hofmann](https://inf.ethz.ch/people/person-detail.hofmann.html)].

Submitted to [[ETH Zürich](https://ethz.ch/en.html)] and [[Imperial College London](https://www.imperial.ac.uk/)] on the 15th of August 2020.

**Thesis Poster**

See the Master_Thesis_Poster.pdf

**Requirements Capture**

1. Implement different model distillation techniques and investigate the factors that contribute to successful knowledge distillation.

2. Research whether the combination of model distillation and parameter reduction (using Filter Pruning) can result in shallow models with small number of parameters and accuracy comparable to complex deep neural networks.

3. Investigate with empirical evidence whether model distillation results in robust student models.

4. Investigate whether model distillation has any effect on the certification area of the models compared to their equivalent complex teacher deep neural networks.

**Model Distillation**

![distillation]

Conclusions:

1)  In order to achieve a high classification accuracy score, the student model needs to be convolutional.

2) The student model needs to be deep: the more convolutional layers, the better the accuracy.

3) Large number of parameters is required to achieve high accuracy score.

3) The shallow student models trained via ”Ranging the Teacher’s Temperature” distillation technique achieve higher accuracy compared with their equivalent networks trained via ”Matching the Logits” distillation technique.

**Filter Pruning**

The method is based on the computation of L1-norm on the different filters. In each layer of the CNN, the sum of its absolute weights is calculated. When a filter is pruned, its feature map and its corresponding kernel in the next convolutional layer are also removed from the new network.

![pruning]

**Adversarial Robustness**

The shallow distillated models (filter pruned) with the best accuracy in both SVHN and CIFAR10 datasets are tested for their out-of-the-box robustness to adversarial non-targeted attacks.. In both datasets for small ε values hence small perturbations, the student model performs better under PGD attacks.

![adversarial]

**Provable Robust Model - Distillation - Certification Area**

![certification]

**Source Files**

The Python / Tensorflow / PyTorch files are now published.

---
