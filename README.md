# BIOS-664-Machine-Learning-with-Health-Sciences

This repo contains homework assignments from University of Michigan Biostatistics course BIOS 664 Machine Learning with Health Sciences.

### Homework 1 Instruction
For this homework, use the R code in the le \simple classication.R" to generate a set of training data.
1. Implement a bootstrap method to estimate the prediction error (EPE) of the linear classier that we used in the class and compare it to the K-fold cross-validation results for K = 2; 5 and 10.
2. For the knn classier that we discussed in the class
(a) Implement a cross-validation scheme select the tuning parameter k, i.e., the "optimal" number of nearest neighbors.
(b) Estimate the EPE for your optimal k using the training data
(c) Simulate new data according to the true generative model and re-estimate the EPE for the estimated optimal k.

3. Find an online tutorial on the R package \caret", study the relevant features and usages of the package
(a) Use caret package to determine the optimal k value for the simple classification example.
(b) Compare the knn classier to the naive Bayes classier implemented in the caret package. Given a brief summary on your conclusions.
