# IRO_VectorBasedRetrievalModel

A vector space model is an algebraic model, involving two steps, in first step we represent the text documents into vector of words and 

in second step we transform to numerical format so that we can apply any text mining techniques

such as information retrieval, information extraction,information filtering etc.

Document vectors representation:

In this step includes breaking each document into words, applying preprocessing steps such as removing stopwords, punctuations, special characters etc.

After preprocessing the documents we represent them as vectors of words.

Next step is to represent the above created vectors of terms to numerical format known as term document matrix. 

Term Document Matrix:

A term document matrix is a way of representing documents vectors in a matrix format in which each row represents term vectors across all the documents 

and columns represent document vectors across all the terms. 

The cell values frequency counts of each term in corresponding document. If a term is present in a document, then the corresponding cell value contains 1 

else if the term is not present in the document then the cell value contains 0.

After creating the term document matrix, we will calculate term weights for all the terms in the matrix across all the documents.

It is also important to calculate the term weightings because we need to find out terms which uniquely define a document. 

Tf-idf = tf X idf 
tf = term frequency is the number of times a term occurs in a document
idf = inverse of the document frequency, given as below
idf = log(N/df), where df is the document frequency-number of documents containing a term

Similarity Measures: cosine similarity

Mathematically, closeness between two vectors is calculated by calculating the cosine angle between two vectors. 

In similar lines, we can calculate cosine angle between each document vector and the query vector to find its closeness. 

To find relevant document to the query term , we may calculate the similarity score between each document vector

and the query term vector by applying cosine similarity .

Finally, whichever documents having high similarity scores will be considered as relevant documents to the query term.

When we plot the term document matrix, each document vector represents a point in the vector space.
