# Topic-Modeling-with-LDA-and-NMF

For this project, Latent Dirichlet Allocation and Non-Negative Matrix Factorization methods are both used to perform unsupervised topic modeling. The models will create a predetermined number of clusters from the articles and questions provided by the datasets, and the user interprets the clusters by assigning topics.


## Dataset and Library
Sci-kit learn was used for this project for its LDA and NMF imports.
The first dataset contains 404288 questions from Quora. The second dataset contains 11992 articles from National Public Radio:
Please find the datasets in the following link:
https://drive.google.com/drive/folders/19HeBmykGvcMKjYxY2cB6v3ae0roMgIwU?usp=sharing 

## Latent Dirichlet Allocation
LDA assumes documents are probability distributions over latent topics. In laymens terms, documents with similar topics ue similar group of words. Moreover, LDA also assumes topics themselves are probability distributions over words. This means latent topics can then be found by searching for groups of words that frequently occur together in documents across the corpus.

## Non-Negative Matrix Factorization
Non-negative Matrix Factorization is an unsupervised algorithm that simultaneously performs dimensionality reduction and clustering. We can use it in conjunction with TF-IDF (term frequency, inverse document frequency) to model topics across documents.

Given a non-negative matrix, A, NMF finds k-dimension approximation in terms of non-negative factors, W and H. Then, NMF approximates each object (i.e. column of A) by a linear combination of k reduced dimensions or “basis vectors” in W. Each basis vector can then be interpreted as a cluster. The memberships of objects in these clusters are encoded by H. In essence, while LDA uses high word frequency to create clusters, NMF uses the calculated word coefficient.

## Results
To see images with the explanations, please visit: https://hjmok.github.io/josephmok_portfolio/#/TM 
### LATENT DIRICHLET ALLOCATION RESULTS
For both the Quora and NPR dataset, LDA was able to cluster 12 and 6 topics respectively. The user interpretation of the resulting clusters appear to be somewhat successful based off the images below.
To improve the model, stricter max and min document frequencies can be used. Also, the user may want to try different number of topics, as 12 may have been too many for Quora due to the larger overlap between topics.

### NON-NEGATIVE MATRIX FACTORIZATION RESULTS
Similar to LDA, the resulting clusters from NMF gave the users some overlapping interpretations. For example, NPR's Article 1 fell under the topic "GOP" in both LDA and NFM, but Article 4 was different between the two.
To further improve the model, NMF experiment with the same parameters listed in LDA above.
