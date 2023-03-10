# iCaRL: Incremental Classifier and Representation Learning
iCaRL paper (arXiv): https://arxiv.org/pdf/1611.07725.pdf

**Incremental learning** is a machine learning paradigm in which a model is trained continuously on new input data whenever it is available, extending the existing model's knowledge.

In this project, three incremental learning methods are implemented and tested: plain Finetuning, Learning-without-Forgetting and iCaRL.

The main focus is on the **iCaRL** framework, which makes use of the techniques of **knowledge distillation** and **prototype rehearsal** to preserve past knowledge acquired by a deep convolutional neural network, while simultaneously training on new classes. An ablation study is performed, experimenting with different combinations of distillation and classification losses and introducing new classifiers. By inspecting the behavior of the newly introduced elements, we seek to better understand how the model benefits from each of its individual components and what its possible weaknesses are.

Subsequently some variations of the original iCaRL algorithm are proposed that attempt to tackle such issues, and their effectiveness is verified. For a fair comparison, tests are performed on the **CIFAR-100 dataset**, as used in the original iCaRL paper. Eventually, the proposed extensions of iCaRL lead to a model achieving a better accuracy than iCaRL on CIFAR-100.

## User guide
- **Baselines**: implementation of Finetuning, Learning-without-Forgetting, iCaRL
- **Ablation study on classifiers**: implementation of iCaRL with four different classifiers for the prediction step (K-nearest neighbors, support vector machines, bias correction layer, cosine normalization layer)
- **Ablation study on losses**: implementation of iCaRL with different classification losses (cross-entropy, binary cross-entropy, mean squared error) and distillation losses (binary cross-entropy, mean squared error, mean absolute error, temperature softmax)
- **Proposals**: proposed variants for the iCaRL framework, namely image augmentation techniques (TenCrop, sample pairing, PatchShuffle, Random Erasing, AutoAugment) and oversampling techniques (SMOTE, random oversampling)
- **Report.pdf**: report for the project, \w results
