Name: Cheitanya Gola
Task: Multi-Level Image Classification Challenge
Dataset: CIFAR-10
_________________________________________
Project Overview
This project demonstrates a progressive, level-wise approach to image classification using deep learning. Starting from a transfer-learning baseline, the system is incrementally improved through data augmentation, learning-rate scheduling, attention mechanisms, and finally expert-level ensemble learning.
Each level introduces a meaningful architectural or training enhancement, supported by quantitative results and qualitative analysis.
________________________________________
Problem Statement
Build a robust image classification system for the CIFAR-10 dataset with increasing model sophistication across multiple levels, aiming to achieve expert-level performance while maintaining interpretability and reproducibility.
________________________________________
Dataset
•	Name: CIFAR-10
•	Images: 60,000 RGB images (32×32)
•	Classes (10):
o	airplane, automobile, bird, cat, deer
o	dog, frog, horse, ship, truck
•	Split:
o	Training: 50,000
o	Test: 10,000
Custom Split Used:
• Training: 40,000 images
• Validation: 10,000 images
• Test: 10,000 images
________________________________________
Methodology & Results
 Level 1 — Baseline Transfer Learning
•	Model: ResNet-18
•	Technique: Transfer learning
•	Accuracy: 90.63%
•	Key Insight: Strong baseline using pretrained features
________________________________________
 Level 2 — Augmentation & Optimization
•	Enhancements:
o	Data augmentation
o	Learning-rate scheduling
o	Improved regularization
•	Model: ResNet-18
•	Accuracy: 93.08%
•	Key Insight: Augmentation significantly improves generalization
________________________________________
 Level 3 — Attention Mechanism
•	Model: SE-ResNet-18
•	Technique: Squeeze-and-Excitation channel attention
•	Accuracy: 94.35%
•	Key Insight: Channel-wise attention improves feature discrimination
________________________________________
 Level 4 — Expert Techniques (Ensemble Learning)
•	Models Used:
o	ResNet-18 (Level-2)
o	SE-ResNet-18 (Level-3)
o	ResNet-34
•	Ensemble Strategy: Soft voting (probability averaging)
•	Final Accuracy: 94.72%
Why Ensemble?
•	Reduces model-specific biases
•	Improves stability and robustness
•	Preserves confidence information via soft voting
________________________________________
Performance Summary
Level	Technique	Accuracy
1	Transfer Learning	90.63%
2	Augmentation + Scheduler	93.08%
3	SE Attention	94.35%
4	Ensemble (Soft Voting)	94.72%
________________________________________
Analysis & Visualizations
•	Per-class accuracy analysis
•	Confusion matrices
•	Error patterns observed in visually similar classes (cat/dog, bird/deer)
•	Ensemble reduces misclassification across difficult categories
________________________________________
Reproducibility
•	Fixed random seeds
•	No hardcoded system-specific paths
•	All experiments executed on Google Colab
•	Models saved and reused for ensemble inference
________________________________________
Google Colab Notebooks
•	Level 1: Baseline Model
•	Level 2: Augmentation & Optimization
•	Level 3: SE Attention
•	Level 4: Ensemble Learning
(Public Colab links included in the submission document)
________________________________________
Limitations & Future Work
Limitations
•	Higher inference cost due to ensemble
•	Increased memory usage
Future Extensions
•	Weighted ensemble strategies
•	Knowledge distillation
•	Robustness testing (noise / adversarial data)
•	Snapshot ensembles
________________________________________
Final Conclusion
This project demonstrates a structured and scalable progression from baseline modeling to expert-level ensemble systems. Each enhancement is justified, measurable, and aligned with real-world machine learning practices.
The final ensemble achieves 94.72% accuracy, meeting expert-level expectations and showcasing strong modeling intuition, experimental discipline, and analytical depth.

