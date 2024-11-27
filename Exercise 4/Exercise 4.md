# Computational Biology

>Unfortunately, the links in this exercise are not working anymore. I haven't saved them locally. If I ever find them somehow, I'll upload them.

For the current assignment we will focus on gene selection, gene annotation and enrichment analysis with visualization.

1. Read the training data from [here](http://139.91.190.186/tei/bioinformatics/LungTrain.txt) and pre-process them in order to create a machine learning model with the sklearn library. You have to transpose the data and set the right label names if you read the file with pandas.
2. Train a SVM model with the training data from step 1 and evaluate your model with the test data that you can find [here](http://139.91.190.186/tei/bioinformatics/LungTest.txt). For the training you will use the full dataset, no split is needed. Print the accuracy and the confusion matrix.
3. Using the attribute coef_[0] of the trained sklearn model you can get the weights assigned to each features/genes. The weights indicate the importance or discriminant power of each gene. Add the coef values to your dataset, short your data and select the first 20 and the last 20 (total 40) genes. Create a heatmap with the 40 genes for the training dataset.
4. Using the library mygene find the annotation of the gene names to the entrez terminology. You can use the function `querymany(genes, scopes = 'reporter', fields='entrezgene', species='human')` where `genes` is a list with your 40 genes.
5. Read the keg human pathways file from [here](http://139.91.190.186/tei/bioinformatics/c2.cp.kegg.v7.4.entrez.gmt). Each row of the file contains information for one KEGG pathway. The file is tab delimited with the first attribute being the pathway name, the second the url and the rest are the genes involved in the specific pathway using the entrez terminology. Find the pathway (or one of the pathways) that contain the most genes from your list of 40 selected genes. Print the pathway name and the genes that are part of the KEGG and belong to the 40 selected.
> If you read the file with pandas, the entrez gene names will be considered from the system as int since these are numbers. On the other hand, the results of querymany function will return information as string. You have to have the same datatype in order to compare. You can use the function int(x) to transform the string to int. 
6. Using the magic cell ***%%HTML*** visualize the selected pathway with the identified genes highlighted. You can create the url hardcoded. In order to find the pathway name (e.g. hsa04012) do a google search with the pathway title as it appears in the file and you will find the pathway name from the url of the specific KEGG map. E.g. https://www.genome.jp/pathway/hsa04012 for ErbB signaling pathway is hsa04012.