# Linear_Regression_CellBox

# Abstract

In this project, we are going to compare the linear regression and CellBox model on a perturbation-response dataset of a 
melanoma cell line after drug treatment. We implemented the linear regression on both random parition, and leave one drug out cases,
the average Pearson's correlations for random partition and leave one drug out from linear regression are better than results from CellBox. 

# How to run 
Download the zip file, and you should able to run all scripts.

# Data description
## There are two data files in this folder

### expert.csv:
Protein expression data from RPPA for the protein nodes and phenotypic node calues. Each row is a condition and each column is a node.

### random_partition_average_testhat_929.csv:
Predicted responses from CellBox model after randomly split the data 1000 times for training and testing

# Code_script description
## There are four coding scripts in this folder

### LR_Random_partition:
In this code script, we predict the cell response on linear regression model, with 70%(n=62 conditions) for training and the rest for testing(30%, n=27 conditions). We repeated this process for 1,000 independent random training and testing datasets, and evaluate the model performance on Pearson's correlation. The average correlation from the linear regression model is 0.962, which is slight higher than the CellBox, 0.926. 

### CellBox_Random_partition:
In this code script, we regenerate the histogram for correlation between CellBox's predictions and experiemtns across all conditions by using their predicted values, "random_partition_average_testhat_929.csv". 

### comparsion:
Generating scatter plots between predicted value from linear regression and CellBox.

### Leave-one_out:
In leave-one-drug-out cross-validation process, all combinations contain the treatment of a particular drug with  were used for testing and the rest of combination were used for training. The average Pearson's correlation from linear regression is 0.784, and the average correlation for CellBox is 0.780.




## References:
Yuan, B., Shen, C., Luna, A., Korkut, A., Marks, D. S., Ingraham, J., & Sander, C. (2021). CellBox: interpretable machine learning for perturbation biology with application to the design of cancer combination therapy. Cell systems, 12(2), 128-140.

CellBox paper github link:https://github.com/sanderlab/CellBox
