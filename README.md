# Code contributions list for the thesis "Comparison between joint and marginal laws for regression and conditional density estimation through label permutations" written by Benjamin Riu at Ecole Polytechnique (to be defended soon). 
par permutation des labels pour la régression
et l’estimation de densité conditionnelle

### (French version below)
### Disclaimer: this is a rough draft containing raw informations about my code contributions in my thesis.

### tl;dr:
| Relevance | Repository |
| ----------- | ----------- |
| Stand-alone, Ch4, Ch5 | [FFNN_InitFitPredict](https://github.com/benjaminriu/FFNN_InitFitPredict) |
| Stand-alone, Ch5 | [MarginalContrastiveDiscrimination](ToBeAdded) |
| Ch3, Ch4 | [MLRTikhAdaCap Demo](ToBeAdded)
| Ch2 | [Step-by-step Deep learning introduction](ToBeAdded) (code in French) |
| Ch3 | [MLR article experiments replication](ToBeAdded)|
| Ch4 | [AdaCap article experiments replication](ToBeAdded)|
| Ch5 | [MarginalContrastiveDiscrimination article experiments replication](ToBeAdded) |
| Stand-alone, Ch2 | [Automated visualization of MLP architectures](ToBeAdded) (code in French) |
| Stand-alone, Ch4, Ch5 | [Continuous target stratification for train_test_split](ToBeAdded) |


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
matplotlib (mandatory), pytorch (mandotory except for a)) 
