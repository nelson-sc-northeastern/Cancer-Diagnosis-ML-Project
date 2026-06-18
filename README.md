This project was during graduate school working directly with a Boston based startup to learn how different machine learning models would be able to predict how 
gene expression data lead to cancer growths. We worked directly with Merek & Co using data they provided across three different sources. 
1. CCLE (Cancer Cell Line Encyclopedia)
2. KO (Knockout)
3. CRISPR (Clustered regularly interspaced short palindromic repeats)

These three data sources provided different data based on how gene dependencies and gene expression.

The starting stage of the project was an indepth analysis of the data and data cleaning. Removing erroneous data and ensuring incomplete data was not in the deployment of the models.

In order to determine the best ML methods for predicting cancer we deployed 5 different methodologies.
1.Logistic Regression: Basic classification alogrithm used as a baseline for binary classification using different iterations on the model we did achieve pretty good results
being able to predict the cancer type from gene data with a .66-.78 accuracy depending on the implementation and dataset.

2.Linear Discriminant Analysis (LDA): Used to find a linear combination of genotypes to determine different cancer classifications. The goal of LDA is to maximize the ratio of the
between-groups variance and within-group variance. The results were a bit weaker than logistic as there were some incorrectly labeled data, which is problematic for LDA. 
Accuracy between .52-.74 depending on the dataset.

3.Clustering: Unsupervised machine learning method that groups unlabeled data into clusters. This method is evaluated by how similar groups are within clusters and how different
between-cluster data is. We also applied PCA for feature selection before the clustering. Overall the results were good with different cancer categories properly clustered together.

4.Random Forest Classifiers: Fits 1 classifier per class. Then using the classifier and data fits each datapoint into a class. Worse performing model with F1 score between .45-.63
depending on the dataset.

5.Neural Networks: Used TensorFlow and Keras were used to build the neural network almost 10m trainable parameters. Had a few issues with overfitting due to a small sample size
for certain classifications of cancer. Combated overfitting using 3 dropout layers. Used a smaller batch size to introduce noise into the training data. Overall results were good
With validation accuracies between .54 - .74 depending on the dataset.

Overall the resuls were great with CRISPR data performing worse than the CCLE dataset. As there were 33 different classifications of cancer a random guess would result in a .033
accuracy as all of the models signifigantly out performed this we know the models are correctly predicitng the data. 


Code is redacted due to data and is available upon request.
