# Code contributions list for the thesis "Comparison between joint and marginal laws through label permutations for regression and conditional density estimation" written by Benjamin Riu at Ecole Polytechnique (to be defended soon). 

### tl;dr:
| Relevance | Repository | language |
| ----------- | ----------- | ----------- |
| Stand-alone, Ch4, Ch5 | [FFNN_InitFitPredict](https://github.com/benjaminriu/FFNN_InitFitPredict) | english |
| Stand-alone, Ch5 | [MarginalContrastiveDiscrimination](ToBeAdded) | english |
| Ch3, Ch4 | [MLRTikhAdaCap Demo](ToBeAdded) | english |
| Ch2 | [Step-by-step Deep learning introduction](ToBeAdded) | French |
| Ch3 | [MLR article experiments replication](ToBeAdded)| english |
| Ch4 | [AdaCap article experiments replication](ToBeAdded)| english |
| Ch5 | [MarginalContrastiveDiscrimination article experiments replication](ToBeAdded) | english |
| Stand-alone, Ch2 | [Automated visualization of MLP architectures](ToBeAdded) | French |
| Stand-alone, Ch4, Ch5 | [Continuous target stratification for train_test_split](ToBeAdded) | english |

### (French version below)
### Disclaimer: this is a rough draft containing raw informations about my code contributions in my thesis.

The goal of this repository is to provide the links and a quick description for the main projects on which I worked during my thesis. Contributions are somewhat sorted by order of importance/usefullness. For backward compatibility and reproductibility reasons there are nearly duplicates of some files with small variations which are explained below. By default stand-alone versions should be prefered. For informations / remarks/ constructive criticisms, do not hesitate to either raise an issue on git or send an email to riubenjamin at gmail dot com.

# Contribution 1 : [FFNN_InitFitPredict](https://github.com/benjaminriu/FFNN_InitFitPredict)
### Type : Stand-alone tool
### Targeted audience
Researchers and Practitionners, python Beginners and Experts. Machine learners and Data-scientists who want an off-the-shelf deep learning solution for supervised-learning in python. Machine learners who want to use the AdaCap training method.
### Description
Implementation of Feed-Forward Neural Networks (FFNNs) training schemes for supervised learning (regression, binary classification, multi-class classification) in python. It combines the ease-of-use of the scikit-learn API and well-chosen default parameters with the efficiency and versatility of the pytorch library. Il also includes a set of recommended architectures and hyper-parameters for a) quick results on tabular datasets; b) high performances on small-to-medium regression tabular datasets; c) high performances on small-to-medium binary classification tabular datasets; d) high performances on large tabular datasets.
### Relation to my thesis
Used in Chapters 4 and 5. Note that this version is made to be a stand-alone tool. The MarginalContrastiveDiscrimination repository contains an exact copy of this code. However, the repositories containing the code to reproduce experiments presented in Chapters 4 and 5 use older versions of this code. These versions correspond to the state in which this project was when the experiments were done. The two biggest differences are that in those versions, AdaCap is the default mode and there is no default architecture provided. 
### Main requirements
pytorch (mandatory), cuda & gpu (optional)


# Contribution 2 : [MarginalContrastiveDiscrimination](ToBeAdded)
### Type : Stand-alone tool
### Targeted audience
Researchers and Practitionners, python Beginners and Experts. Machine Learners, Data-scientists and Statisticians who want a one-size-fits-all state-of-the-art non-parametric solution for conditional density estimation in python.
### Description
Implementation of the Marginal Contrastive Discrimination (MCD) method for conditional density estimation (CDE) in python. It is compatible with any regressor or binary classifier which implements "\_\_init\_\_()", "fit(X, y)", "predict(X)"/"predict\_proba(X)" (eg: scikit-learn, xgboost, catboost, FFNN_InitFitPredict). It also provides a straight-forward and unified API for the CDE task inspired from scikit-learn for both density estimators ("\_\_init\_\_()", "fit(X, y)", "pdf\_from\_X(X)") and density models (generate\_X(), generate\_y\_from\_X(X), "evaluate_divergences(estimator)"). 
### Relation to my thesis
Used in Chapter 5. Note that this version is made to be a stand-alone tool. The repository containing the code to reproduce experiments presented in Chapter 5 uses an older version of this code. That version corresponds to the state in which this project was when the experiments were done. The biggest difference is that some features which were later abandonned are still present in the old version, and some function were renamed.
### Main requirements
scikit-learn (mandatory), FFNN_InitFitPredict (optional), catboost (optional)

# Contribution 3 : [MLRTikhAdaCap Demo](ToBeAdded)
### Type : Tutorial
### Targeted audience
Researchers, python Beginners and Experts. Machine Learners and Statisticians who want a quick introduction to the Muddling Label Regularization (MLR) criterion, the Tikhonov operator (Tikh.) and the Adaptative Capacity Control (AdaCap) training scheme.
### Description
A set of Jupyter Notebooks showing the behavior and impact when using MLR, Tikh. and AdaCap. It includes a) a comparison between MLR and Cross-Validation in a toy Ridge Linear Regression setting; b) a comparison between MSE, Tikh. and AdaCap in terms of learning dynamic on the Boston dataset; c) a comparison between Weight-Decay, Tikh. and AdaCap in terms of hidden layers weights covariance structure on the Boston dataset; d) a comparison between RMSE and AdaCap for few-shot learning on MNIST.
### Relation to my thesis
Quick empirical introduction/recap of the experiments and intuitions presented in Chapters 1, 3 and 4. Note that the implementation of AdaCap here does not correspond to the stand-alone FFNN_InitFitPredict but instead to AdaCap article experiments replication. The main reason is that some notebooks are duplicates from the two repositories.
### Main requirements
matplotlib (mandatory), pytorch (mandotory except for a)) , cuda & gpu (optional)

# Contribution 4 : [Step-by-step Deep learning introduction](ToBeAdded)
### Type : Tutorial
### Targeted audience
French students, python Beginners. Readers of Chapter 2 of the thesis.
### Description
A Jupyter Notebooks providing the code extracts included in Chapter 2, which is a step-by-step introduction to deep learning from linear regression in french. Originality of the tutorial is that a) the code is also written in French from A to Z, b) variable names correspond to the notations used in the corresponding Chapter, c) it requires minimal set up and proficiency in python as the only required library is numpy.
### Relation to my thesis
It corresponds to the code extracts provided in Chapter 2, with some minor changes corresponding to corrections. 
### Main requirements
numpy (mandatory)

# Contribution 5 : [MLR article experiments replication](ToBeAdded)
### Type : Supplementary material
### Targeted audience
Researchers, python non-Beginners. Referees of Chapter 3 of the thesis or the corresponding article submissions. 
### Description
A github repository containing instructions and source code to replicate the experiments presented in Chapter 3.
### Relation to my thesis
It corresponds to the figures, tables, experiments section and appendix section of Chapter 3. Minor changes correspond to cosmetic improvement for readability, but the goal is that results are equal or as close as possible to the original version. Recorded times will vary with the machine used of course. 
### Main requirements
scikit-learn (mandatory)

# Contribution 6 : [AdaCap article experiments replication](ToBeAdded)
### Type : Supplementary material
### Targeted audience
Researchers, python non-Beginners. Referees of Chapter 4 of the thesis or the corresponding article submissions. 
### Description
A github repository containing instructions and source code to replicate the experiments presented in Chapter 4. Code to generate figures is provided in notebooks and may take at most a few minutes to run (with a gpu). Code to replicate benchmark is provided in bash and python and may take at least a few days to run (with a HPC cluster).
### Relation to my thesis
It corresponds to the figures, tables, experiments section and appendix section of Chapter 4. Minor changes correspond to cosmetic improvement for readability, but the goal is that obtained results are equal or as close as possible to the original version. Recorded times will vary with the machine used of course. 
### Main requirements
pytorch, catboost, xgboost, lightgbm, py-earth (mandatory), cuda & gpu & a cluster (optional)

# Contribution 7 : [MarginalContrastiveDiscrimination article experiments replication](ToBeAdded)
### Type : Supplementary material
### Targeted audience
Researchers, seasoned python practionners. Referees of Chapter 5 of the thesis or the corresponding article submissions. 
### Description
A github repository containing instructions and source code to try to replicate the experiments presented in Chapter 5. Please note that a) it is not possible to obtain the exact results depicted in the corresponding paper for all benchmarked methods for reasons detailed in the "Relation to my thesis" paragraph below, b) it is very hard to run all the experiments in one go for reasons detailed in the "Main requirements" paragraph below. However, these issues concern results from other methods, results obtained with MCD are fully reproducible. 
### Relation to my thesis
It corresponds to the figures, tables, experiments section and appendix section of Chapter 5. Major changes correspond to increased reproductibility. Minor changes correspond to cosmetic improvements for readability. For some methods (but not MCD), it is not actually possible to completely control the sources of randomness by fixing the value of the seed. In these cases, results might vary (but I do not think this could lead to major changes in how the results should be interpreted). Likewise, recorded times for some methods will vary greatly between runs, even on the same machine. See the repository README.md file for more details. 
### Main requirements
Advanced knowledge on how cuda, tensorflow, edward and pytorch interact with each other, how compatibility issues between packages can be solved, and how to manually change source code from a library. See the repository README.md file for more details.

# Contribution 8 (minor) : [Automated visualization of MLP architectures](ToBeAdded)
### Type : Stand-alone tool
### Targeted audience
Teachers, python Beginners and Experts. People who are creating teaching material for deep learning courses. Code is a mixture of french, english and frenglish, but speaking any of the two languages should be sufficient.
### Description
Quick tool to generate in python good looking visualizations of multilayer perceptrons with varying width and depth. Activation functions are provided as python functions, and their representations are generated dynamically.
### Relation to my thesis
Used to generate a figure in Chapter 2. Notations used correspond to those used in Chapter 2. Input arguments correspond to those used in the Step-by-step Deep learning introduction project.
### Main requirements
matplotlib (mandatory)

# Contribution 9 (minor) : [Continuous target stratification for train_test_split](ToBeAdded)
### Type : Stand-alone tool
### Targeted audience
Teachers, python Beginners and Experts. People who are creating teaching material for deep learning courses.
### Description
Simple function to stratify a continuous vector, such that the train_test_split function from scikit-learn will generate splits with balanced repartition of high and low target values in each fold. It is included in the FFNN_InitFitPredict project but can have other applications besides deep learning. It is partially based on an answer from cross-validated.com
### Relation to my thesis
It is one part of the "FeedForwardNeuralNetwork" class, which is used in Chapter 4 and 5. 
### Main requirements
scikit-learn (mandatory)
