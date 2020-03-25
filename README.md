# BIOS-664-Machine-Learning-with-Health-Sciences

This repo contains homework assignments from University of Michigan Biostatistics course BIOS 664 Machine Learning with Health Sciences.

## Homework 1 Instruction
For this homework, use the R code in the "simple classification.R" to generate a set of training data.
#### Problems
1. Implement a bootstrap method to estimate the prediction error (EPE) of the linear classier that we used in the class and compare it to the K-fold cross-validation results for K = 2; 5 and 10.
2. For the knn classifier that we discussed in the class
(a) Implement a cross-validation scheme select the tuning parameter k, i.e., the "optimal" number of nearest neighbors.
(b) Estimate the EPE for your optimal k using the training data
(c) Simulate new data according to the true generative model and re-estimate the EPE for the estimated optimal k.

3. Find an online tutorial on the R package \caret", study the relevant features and usages of the package
(a) Use caret package to determine the optimal k value for the simple classification example.
(b) Compare the knn classier to the naive Bayes classier implemented in the caret package. Given a brief summary on your conclusions.


## Homework 2 Instruction
The primary goal of this assignment is to construct linear prediction algorithms to predict gene expression levels using genetic variants. 

The whole data set contains text formatted data files for 2 genes: ENSG00000238142.1 and ENSG00000146574.15, as indicated by the corresponding file names. There are 3 separate files for each gene:
1. genotype data for training samples (named as `ENSG###.training_geno.dat` ): genotype data matrix (Nxp) for a given gene. For all genes, training data sample size N=570. The numbers of candidate SNPs ( i.e., the predictors) are 5230 and 7788 for ENSG00000238142.1 and ENSG00000146574.15, respectively. 

2. normalized expression level data for training samples (named as ENSG###.training_pheno.dat ): gene expression data matrix (Nx1) for a given gene, the data are normalized by certain procedures to reflect the relative rank of the actual gene expression levels and allow negative values.  

3. genotype data for testing samples (named as `ENSG###.testing_geno.dat`): genotype data matrix (M x p) for a given gene. For all genes, testing data sample size M=100. This genotype data file also contains a header of SNP names. The number and position of SNPs are matched in training and testing data.  


#### Problems
1. Fit the two training datasets by finding a prediction function containing only a single best predictor/SNP. Record this set of the prediction functions as `predict_single`.  

2. Find the best subset of predictors using forward (or backward, or forward-backword) subset selection algorithms. Fit the two training datasets with your best subset predictors. Record this set of prediction functions as `predict_stepwise`.  

3. Fit the two training datasets by the Lasso regression algorithm. Describe how the tuning parameters are selected. Record this set of prediction functions as `predict_lasso`. 

4. Fit the two training datasets by the ridge regression algorithm. Describe how the tuning parameters are selected. Record this set of prediction functions as `predict_ridge`.  

5. Fit the two training datasets by the elastic-net regression algorithm. Describe how the tuning parameters are selected. Record this set of prediction functions as `predict_enet`.  

6. Comments on the prediction functions you have constructed from 1 - 5. Which prediction function do you expect to have the best performance on the testing data? Why?  

7. Apply the prediction functions constructed from 1 - 5 to corresponding testing data set. Organize your prediction results into a text file (space or tab delimited) using the following format with the appropriate header:  
 `predict_single predict_stepwise ... predict_enet val_ind_1_by_single ...` 
  `val_ind_2_by_single ......val_ind_100_by_single ...`  

## Homework 3 Instruction
In this assignment, we will solve a classification problem using the Caravan dataset including in the R library `ILSR`. This data set includes 85 predictors that measure demographic characteristics for 5,822 individuals. The binary response variable (last column of the data matrix) is Purchase, which indicates whether or not a given individual purchases a caravan insurance policy. In this data set, only 6% of people purchased caravan insurance.

#### Problems
1. Train the following ML algorithms on the training datasets, compute the expected classification errors for each method using cross-validation.
• logistic regression
• linear discriminant analysis
• support vector machine with linear kernel
• support vector machine with radial kernel
• feed-forward neural network (single or multiple hidden layers)
• AdaBoost 

2. Evaluate the classification algorithms on the testing dataset. Are the expected classification errors computed above accurate?
3. Build a best ensemble classifier using the existing built classifiers from question 1. Is the performance better?
4. Comment on/propose possible approaches to improve the classifier.





