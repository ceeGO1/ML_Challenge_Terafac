**Multi-Level Image Classification Challenge**

Name: Cheitanya Gola
Dataset: CIFAR-10

___________________________________________________________________

**Project Overview**

This project follows a level-wise approach to image classification, where the model is gradually improved through architectural and training enhancements. Starting with a transfer-learning baseline, successive levels introduce data augmentation, optimization techniques, attention mechanisms, and finally ensemble learning.

The goal was not only to improve accuracy but also to understand how each modification affects model behavior and performance.

___________________________________________________________________

**Problem Statement**

The objective is to build a reliable image classification system for the CIFAR-10 dataset, improving performance step by step while keeping the experiments reproducible and the results interpretable.

___________________________________________________________________

**Dataset**

Dataset: CIFAR-10
Total Images: 60,000 RGB images (32 × 32)
Classes:
airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck

___________________________________________________________________

**Dataset Split**

Original training set: 50,000 images

Test set: 10,000 images

Split Used in This Project

Training: 40,000 images

Validation: 10,000 images

Test: 10,000 images

A separate validation set was created from the training data to monitor performance and avoid overfitting.

___________________________________________________________________

**Methodology and Results**

Level 1 — Transfer Learning Baseline

Model: ResNet-18

Approach: Transfer learning using pretrained weights

Test Accuracy: 90.63%

This level establishes a strong baseline by leveraging pretrained features, which perform well even with minimal tuning.

Level 2 — Data Augmentation and Optimization

Improvements Introduced:

Random cropping and horizontal flipping

Learning-rate scheduling

Better regularization

Model: ResNet-18

Test Accuracy: 93.08%

Data augmentation significantly improved generalization and reduced overfitting compared to the baseline model.

Level 3 — Channel Attention

Model: SE-ResNet-18

Technique: Squeeze-and-Excitation blocks

Test Accuracy: 94.35%

Adding channel-wise attention helped the network focus on more informative features, leading to consistent gains across most classes.

Level 4 — Ensemble Learning

Models Combined:

ResNet-18 (Level 2)

SE-ResNet-18 (Level 3)

ResNet-34

Method: Soft voting using averaged class probabilities

**Final Accuracy: 94.72%**

The ensemble reduces individual model biases and improves stability, especially on visually similar classes.

___________________________________________________________________

**Performance Summary**

Level,    	Technique,	                 Accuracy

1,	     Transfer Learning,              	90.63%

2,	     Augmentation & Scheduling,      	93.08%

3,	     SE Attention,	                   94.35%

4,	     Ensemble (Soft Voting),         	94.72%

___________________________________________________________________

**Analysis and Observations**

Confusion matrices show fewer errors between vehicle classes in higher levels

Classes such as cat and dog remain challenging, but ensemble learning reduces misclassification

Attention and ensemble methods complement each other well

___________________________________________________________________

**Reproducibility**

Fixed random seeds were used

Experiments were run on Google Colab

Trained models were saved and reused for ensemble inference

No system-specific paths were hardcoded

___________________________________________________________________

**Colab Notebooks**

Separate notebooks were maintained for each level:

Level 1: Baseline model : https://colab.research.google.com/drive/1h3g1Jpm01ec6sVbNl4_uOJElTL7Ck9i2?usp=sharing

Level 2: Augmentation and optimization : https://colab.research.google.com/drive/1mHSTYNe-_IfQtwMauUqSu-Q2CXIhHrx_?usp=sharing

Level 3: Attention-based model : https://colab.research.google.com/drive/14NF2WKDSaSxABlQ6b8kBUJIdR--dratj?usp=sharing

Level 4: Ensemble learning : https://colab.research.google.com/drive/1jNy-UoS0N5bcgZO1IlwLfJ6Vm7076s26?usp=sharing

___________________________________________________________________

**Limitations and Future Scope**

**Current Limitations**

Higher inference time due to multiple models

Increased memory usage

**Possible Extensions**

Weighted ensemble based on validation performance

Knowledge distillation to compress the ensemble

Robustness testing under noise or adversarial conditions


**Final Remarks**

This project demonstrates a clear progression from a simple baseline to an expert-level ensemble system. Each improvement was guided by experimentation and analysis rather than trial-and-error.

The final ensemble model achieves 94.72% accuracy, meeting the expected expert-level threshold and reflecting a strong understanding of modern deep learning practices.
