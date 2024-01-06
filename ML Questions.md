- [What does it mean for learning to be supervised?](#what-does-it-mean-for-learning-to-be-supervised)
- [What does it mean for learning to be unsupervised?](#what-does-it-mean-for-learning-to-be-unsupervised)
- [What is an epoch?](#what-is-an-epoch)
- [What is a minibatch?](#what-is-a-minibatch)
- [Why do we use separate training and test sets?](#why-do-we-use-separate-training-and-test-sets)
- [What is a classification problem?](#what-is-a-classification-problem)
- [When do we use the sigmoid activation function?](#when-do-we-use-the-sigmoid-activation-function)
- [When do we use the softmax activation function?](#when-do-we-use-the-softmax-activation-function)
- [What is the definition of the ReLU activation function?](#what-is-the-definition-of-the-relu-activation-function)
- [When do we use the ReLU activation function?](#when-do-we-use-the-relu-activation-function)
- [When do we use the binary cross-entropy loss function?](#when-do-we-use-the-binary-cross-entropy-loss-function)
- [When do we use the categorical cross-entropy loss function?](#when-do-we-use-the-categorical-cross-entropy-loss-function)
- [What would be the activation function and loss for a binary classification problem?](#what-would-be-the-activation-function-and-loss-for-a-binary-classification-problem)
- [What would be the activation function and loss for a multiclass classification problem?](#what-would-be-the-activation-function-and-loss-for-a-multiclass-classification-problem)
- [Which of these are stopwords?](#which-of-these-are-stopwords)
- [Which of these words were stemmed?](#which-of-these-words-were-stemmed)
- [What does a language model do?](#what-does-a-language-model-do)
- [What is the bag of words model?](#what-is-the-bag-of-words-model)
- [What is the difference between bag of words and TFIDF?](#what-is-the-difference-between-bag-of-words-and-tfidf)
- [What kind of hyperplane is the Support Vector Machine (SVM) learning?](#what-kind-of-hyperplane-is-the-support-vector-machine-svm-learning)
- [What do we use the confusion matrix for?](#what-do-we-use-the-confusion-matrix-for)
- [What is grid search? Why do we use it?](#what-is-grid-search-why-do-we-use-it)
- [When would you use random search instead of grid search?](#when-would-you-use-random-search-instead-of-grid-search)
- [What would be the one-hot encoding of \[1, 3, 0\]?](#what-would-be-the-one-hot-encoding-of-1-3-0)
- [What does a word embedding do?](#what-does-a-word-embedding-do)
- [What is an example of clustering?](#what-is-an-example-of-clustering)
- [What is the difference between hard and soft clustering?](#what-is-the-difference-between-hard-and-soft-clustering)
- [What is NOT true of the k-means problem?](#what-is-not-true-of-the-k-means-problem)
- [What is NOT an issue with the k-means algorithm?](#what-is-not-an-issue-with-the-k-means-algorithm)
- [What does Latent Semantic Analysis do?](#what-does-latent-semantic-analysis-do)
- [What is NOT a reason to use dimensionality reduction?](#what-is-not-a-reason-to-use-dimensionality-reduction)
- [What is a principal component in Principal Components Analysis (PCA)?](#what-is-a-principal-component-in-principal-components-analysis-pca)
- [What is the relationship between Principal Component Analysis (PCA) and Singular Value Decomposition (SVD)?](#what-is-the-relationship-between-principal-component-analysis-pca-and-singular-value-decomposition-svd)
- [Why doesn’t the autoencoder just do an identity transformation?](#why-doesnt-the-autoencoder-just-do-an-identity-transformation)
- [How many matrices does Latent Semantic Analysis produce from its input matrix?](#how-many-matrices-does-latent-semantic-analysis-produce-from-its-input-matrix)


### What does it mean for learning to be supervised?

Supervised learning is a subcategory of machine learning and artificial intelligence that uses labeled datasets to train algorithms to classify or predict data.

### What does it mean for learning to be unsupervised?

Unsupervised learning is a machine learning technique that uses algorithms to analyze and cluster unlabeled datasets.

### What is an epoch?

An epoch is a training pass on the whole train set.

### What is a minibatch?

A minibatch is a small portion of a training set. It's used in mini-batched gradient descent, which performs gradient descent on small matches of the dataset.

### Why do we use separate training and test sets?

Because we want to be able to test the performance of our model on data that it has never seen before. It helps detect performance issues and overfitting.

### What is a classification problem?

A classification problem is a problem in which machines have to group data together by a particular criteria.

### When do we use the sigmoid activation function?

We use the sigmoid activation function to convert values that are outside the range (0, +1) into this range.

### When do we use the softmax activation function?

It is used to transform a vector into a normalized probability distribution consiting of the same number of probabilities as the length of the input vector. Can be used in classification problems with 2+ classes.

### What is the definition of the ReLU activation function?

$$
    ReLU(x) = max(0, x)
$$

### When do we use the ReLU activation function?

We use ReLU whenever we wish to drop all the negative values from a layer in a model.

### When do we use the binary cross-entropy loss function?

Binary cross-entropy loss is used whenever you need to compute the loss of a binary classification model's predictions.

### When do we use the categorical cross-entropy loss function?

We use this function whenever we need to compute the loss for the predictions of a classification model in a problem with 2 > classes.

### What would be the activation function and loss for a binary classification problem?

Activation function: Sigmoid

Loss function: Binary cross-entropy

### What would be the activation function and loss for a multiclass classification problem?

Activation function: Softmax

Loss function: Categorical cross-entropy

### Which of these are stopwords?

Stopwords are words which are very commonly used in a language but provide very little useful information. Some stopwords are "a," "the," "is," "are," etc.

### Which of these words were stemmed?

Stemmed words are words who are put in their root form, with their suffix removed.
Example:
"cats", "catty", "catlike" become "cat" after stemming.

The stem need not be a word, for example the Porter algorithm reduces argue, argued, argues, arguing, and argus to the stem argu. 

### What does a language model do?

A language model is a machine learning model that aims to predict and generate plausible language.

### What is the bag of words model?

The bag-of-words model is a model of text which uses a representation of text that is based on an unordered collection of words. It is called a “bag” of words, because any information about the order or structure of words in the document is discarded. The model is only concerned with whether known words occur in the document, not where in the document.

### What is the difference between bag of words and TFIDF?

Bag of words simply counts the frequency of words in a document, which can lead to stop words having a higher count value hence giving them extra importance (this can be avoided by removing the stop words). TF-IDF does not have this problem, as words that are common in all documents have a much lower score than rarer words, making them less important in a mathematically elegant way.

### What kind of hyperplane is the Support Vector Machine (SVM) learning?

It is learning the optimal hyperplane that separates data points of different classes with maximum margin. The hyperplane serves as the decision boundary, enabling SVMs to make predictions on unseen data.

### What do we use the confusion matrix for?

To have a view of the correct and incorrect predictions a model makes and the type of incorrect predictions it makes.

### What is grid search? Why do we use it?

Grid search is a hyperparameter optimization technique which tries out different values for different hyperparamteres out of a "search grid" and ultimately selects the values for which the model performs best.

### When would you use random search instead of grid search?

When you want to save up on computational power and you have a huge search grid. The results of random search run in 60 iterations has a 95% chance of landing on a top 5% hyperparameter configuration.

### What would be the one-hot encoding of [1, 3, 0]?

[0,1,0,0]\
[0,0,0,1]\
[1,0,0,0]

### What does a word embedding do?

A word embedding is a representation of a word. Typically, the representation is a real-valued vector that encodes the meaning of the word in such a way that the words that are closer in the vector space are expected to be similar in meaning.

### What is an example of clustering?

1. Image segmentation
2. Anomaly detection
3. Grouping stars by brightness
4. Grouping documents by topic
5. Grouping organisms by genetic information into a taxonomy

### What is the difference between hard and soft clustering?

Hard clustering only assigns elements to one cluster, while soft clustering allows elements to exist in multiple clusters by providing a probability that a data point belongs in the assigned clusters.

### What is NOT true of the k-means problem?

The k-means problem:

$$
\argmin_S \sum_{i = 1}^{k}\sum_{x \in S_i} || x -\mu ||^2
$$

Given k, find the k centroids $\mu$ which minimize the mean squared error of the elements of each cluster $S_i$ from it's centroid $\mu_i$.

### What is NOT an issue with the k-means algorithm?

Some issues are:
- The k can be too small
- The k can be too large
- The centroids can be poorly initialized
- Sometimes the clusters are not centroid based

### What does Latent Semantic Analysis do?

Is a NLP techinque of analyzing relationships between a set of documents and the terms they contain by producing a set of concepts related to the documents and terms. It assumes that words that are close in meaning will occur in similar pieces of text.

### What is NOT a reason to use dimensionality reduction?

You would want to use dimensionality reduction when:
- You want to reduce the computational complexity of working with a dataset
- You want to visualize a dataset in fewer dimensions

### What is a principal component in Principal Components Analysis (PCA)?

A principal component is a vector which maximizes the variance of a dataset in a direction. (Maybe)

Wikipedia definition: "The principal components of a collection of points in a real coordinate space are a sequence of p p unit vectors, where the $i$-th vector is the direction of a line that best fits the data while being orthogonal to the first $i-1$ vectors."

### What is the relationship between Principal Component Analysis (PCA) and Singular Value Decomposition (SVD)?

One way to perform PCA is to perform SVD on the data set, this method does not use the covariance matrix.

### Why doesn’t the autoencoder just do an identity transformation?

Because the input gets compressed into a much smaller dimension causing data loss, and then gets decompressed again making the output different from the input, but with the same dimension.

### How many matrices does Latent Semantic Analysis produce from its input matrix?

3
- $\hat{U}^{topics \times words}$
- $\hat{S}^{topics \times topics}$
- $\hat{V}^{T, topics \times documents}$