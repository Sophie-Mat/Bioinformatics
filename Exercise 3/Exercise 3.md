# Gene expression analysis (statistics and machine learning)

For the current assignment we will focus on gene expression data. The data file that we will use can be found [here](http://139.91.190.186/tei/bioinformatics/exercise3/GDS4794.txt). It is a tab delimited gene expression data from healthy and small cell lung cancer (SCLC) tissues for which we will implement a data analysis script with the following steps:

> Update: Unfortunately the link above is not working anymore and I
> haven't saved the file locally.


## 1. Data pre-processing

 1. Read the data file and store it in a dataframe.
 2. Select the 10 first and 10 last genes (rows) and create a heatmap. Make sure not to visualize the first column which is the gene/probeID name.
 3. Find the mean value of the SCLC samples per row (gene), the mean value of the normal samples and their difference. Then select only the samples with absolute value in the difference that is over 1. Store the selected data in a new dataframe. After that step your rows should be reduced to 12506.

## 2. Statistical analysis

1. Find the p-value of all the genes based on the two classes. Be careful not to use any columns you have created such as means or differences.
2. Select only the genes/rows that their p-value is less than 0.0000004 (that’s the Bonferroni corrected p-value for 0.05) and with absolute difference at the means over 4.
3. Sort your selected data based on the differences and create a heatmap using only the first 10 and the last 10 genes.

## 3. Machine learning analysis

1. We will use the dataset from step 1.3 (12460 rows/genes). To use machine learning for gene expression data you must set your genes/features to columns and the samples to rows. So, you must transpose your dataset. Furthermore, store your gene names to a new list, your sample classes to a new list (your sample classes are only two, remove any numbering that the dataframe added for unique names of the columns) and your data without the gene names and without the means, differences etc to a new dataframe. Then use the function train_test_split with random_state=2 to split your data to train and test with test size = 0.25 .
2. Train a decision tree model using the training data from the split at the previous step and predict the class for the test data. Visualize the tree, print the confusion matrix and the accuracy of the model.
3. Train a Support Vector Machines model using the training data from the split at the previous step and predict the class for the test data. Print the confusion matrix and the accuracy of the model.
