# Build-a-TFIDF-Vectorizer-compare-its-results-with-Sklearn

As a part of this we have implementing TFIDF vectorizer on a collection of text documents.

We have compare the results of your own implementation of TFIDF vectorizer with that of sklearns implemenation TFIDF vectorizer.

Sklearn does few more tweaks in the implementation of its version of TFIDF vectorizer, so to replicate the exact results you would need to add following things to your custom implementation of tfidf vectorizer:
Sklearn has its vocabulary generated from idf sroted in alphabetical order
Sklearn formula of idf is different from the standard textbook formula. Here the constant "1" is added to the numerator and denominator of the idf as if an extra document was seen containing every term in the collection exactly once, which prevents zero divisions.
𝐼𝐷𝐹(𝑡)=1+log𝑒1 + Total number of documents in collection1+Number of documents with term t in it.
 

Sklearn applies L2-normalization on its output matrix.
The final output of sklearn tfidf vectorizer is a sparse matrix

Steps to approach this task:
1.You would have to write both fit and transform methods for your custom implementation of tfidf vectorizer.
2.Print out the alphabetically sorted voacb after you fit your data and check if its the same as that of the feature names from sklearn tfidf vectorizer.
3.Print out the idf values from your implementation and check if its the same as that of sklearns tfidf vectorizer idf values.
4.Once you get your voacb and idf values to be same as that of sklearns implementation of tfidf vectorizer, proceed to the below steps.
5.Make sure the output of your implementation is a sparse matrix. Before generating the final output, you need to normalize your sparse matrix using L2 normalization. 6.You can refer to this link https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.normalize.html
7.After completing the above steps, print the output of your custom implementation and compare it with sklearns implementation of tfidf vectorizer.
8.To check the output of a single document in your collection of documents, you can convert the sparse matrix related only to that document into dense matrix and print it.
