# Analysis of Popular ML Papers

I conducted an analysis to identify topics in popular Machine Learning papers submitted to the NIPS (Neural Information Processing Systems) conference, https://nips.cc/. 

## Keywords: 
  Latent Dirichlet Allocation (LDA), Topic Modeling, Natural Language Processing, Data Visualization

## Libraries Used: 
1. Regular Expression 
2. Pandas 
3. CountVectorizer
4. LatentDirichletAllocation
5. Numpy

## Steps followed:
**1. Preparing the data for analysis by removing columns that aren't required.**

**2. Plotting the evolution of ML over the years:**

   This is done by plotting a bar chat showing the number of papers submitted every year from 1987 to 2017. We can see a steady increase in the number of papers submitted.  Another observation here is a sudden spike in the number of papers submitted from 2016. 

![Barchart](/Images/EvolutionOfML.png)

**3. Preprocessing the data:**

The data is preprocessed to remove punctuations, stop words; and is also converted to lower case. 

**4. Word Cloud to visualize the preprocessed data**

A word cloud is then displayed to show common words used in all the titles. 

![WordCloud](/Images/WordCloud.png)

**5. Preparing the text for LDA Analysis**

The main text analysis method that we will use is latent Dirichlet allocation (LDA). LDA is able to perform topic detection on large document sets, determining what the main 'topics' are in a large unlabeled set of texts. A 'topic' is a collection of words that tend to co-occur often. 

LDA does not work directly on text data. First, it is necessary to convert the documents into a simple vector representation. We will convert a list of titles into a list of vectors, all with length equal to the vocabulary. For example, 'Analyzing machine learning trends with neural networks.' would be transformed into [1, 0, 1, ..., 1, 0].

We'll then plot the 10 most common words based on the outcome of this operation.

![WordCloud](/Images/MostCommonWords.png)

**6. Analysing Trends with LDA**

Finally, the research titles will be analyzed using LDA. One obvious improvement to my code is to do something similar to a grid search to tune the number of words and number of topics. These can be tweaked, iterating over different combinations of these to find the combination with the lowest 'perplexity'. 


