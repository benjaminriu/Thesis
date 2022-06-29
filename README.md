# Contribution list

### (French version below)
### Disclaimer: this is a rough draft containing raw informations about my code contributions in my thesis.

### tl;dr:
- Stand-alone, Ch4, Ch5 : [FFNN_InitFitPredict](https://github.com/benjaminriu/FFNN_InitFitPredict)
- Stand-alone, Ch5 : [MarginalContrastiveDiscrimination](ToBeAdded)
- Ch3, Ch4 : [AdaCap Demo](ToBeAdded)
- Ch2 : [Step-by-step Deep learning introduction](ToBeAdded) (code in French)
- Ch3 : [MLR article experiments replication](ToBeAdded)
- Ch4 : [AdaCap article experiments replication](ToBeAdded)
- Ch5 : [MarginalContrastiveDiscrimination article experiments replication](ToBeAdded)
- Stand-alone, Ch2 : [Automated visualization of MLP architectures](ToBeAdded) (code in French)
- Stand-alone, Ch4, Ch5 : [Continuous target stratification for train_test_split](ToBeAdded)


The goal of this repository is to provide the links and a quick description for the main projects on which I worked during my thesis. For informations do not hesitate to either raise an issue on git or send an email to riubenjamin at gmail dot com. Contributions are somewhat sorted by order of importance/usefullness. 


# Contribution 1 : [FFNN_InitFitPredict](https://github.com/benjaminriu/FFNN_InitFitPredict)
### Type : Stand-alone tool
### Targeted audience
Academic & Industry, Beginners and Experts. Machine learners who want an off-the-shelf deep learning solution for supervised-learning in python. Machine learners who want to use the AdaCap training method.
### Description
Implementation of Feed-Forward Neural Networks (FFNNs) training schemes for supervised learning (regression, binary classification, multi-class classification). It combines the ease-of-use of the scikit-learn API and well-chosen default parameters with the efficiency and versatility of the pytorch library.
### Relation to my thesis
Used in Chapters 4 and 5. Note that this version is made to be a stand-alone tool. The MarginalContrastiveDiscrimination repository contains an exact copy of this code. However, the repositories containing the code to reproduce experiments presented in Chapters 4 and 5 use older versions of this code. These versions correspond to the state in which this project was when the experiments were done. The two biggest differences are that in those versions, AdaCap is the default mode and there is no default architecture provided. 
### Main requirements :
pytorch (mandatory), cuda & gpu (optional)


# Contribution 2 : [MarginalContrastiveDiscrimination](ToBeAdded)
### Type : Stand-alone tool
### Targeted audience
Academic & Industry, Beginners and Experts. Machine Learners and Statisticians who want a one-size-fits-all state-of-the-art non-parametric solution for conditional density estimation in python.
### Description
Implementation of Feed-Forward Neural Networks (FFNNs) training schemes for supervised learning (regression, binary classification, multi-class classification). It combines the ease-of-use of the scikit-learn API and well-chosen default parameters with the efficiency and versatility of the pytorch library.
### Relation to my thesis
Used in Chapter 5. Note that this version is made to be a stand-alone tool. Note however that, the repository containing the code to reproduce experiments presented in Chapter 5 uses an older version of this code. This version corresponds to the state in which this project was when the experiments were done. The biggest difference is that some features which were later abandonned are still present in the old version.
### Main requirements :
scikit-learn (mandatory), FFNN_InitFitPredict (optional), catboost (optional)

# Contribution 3 : [MarginalContrastiveDiscrimination](ToBeAdded)
### Type : Stand-alone tool
### Targeted audience
Academic & Industry, Beginners and Experts. Machine Learners and Statisticians who want a one-size-fits-all state-of-the-art non-parametric solution for conditional density estimation in python.
### Description
Implementation of Feed-Forward Neural Networks (FFNNs) training schemes for supervised learning (regression, binary classification, multi-class classification). It combines the ease-of-use of the scikit-learn API and well-chosen default parameters with the efficiency and versatility of the pytorch library.
### Relation to my thesis
Used in Chapter 5. Note that this version is made to be a stand-alone tool. Note however that, the repository containing the code to reproduce experiments presented in Chapter 5 uses an older version of this code. This version corresponds to the state in which this project was when the experiments were done. The biggest difference is that some features which were later abandonned are still present in the old version.
### Main requirements :
scikit-learn (mandatory), FFNN_InitFitPredict (optional), catboost (optional)
