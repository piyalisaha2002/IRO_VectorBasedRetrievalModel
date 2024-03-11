# Vector-Based Retrieval Model

The Vector-Based Retrieval Model is an algebraic model used for information retrieval, information extraction, and information filtering tasks. It involves representing text documents as vectors of words and transforming them into a numerical format for further analysis. This project implements the vector space model to facilitate efficient document retrieval and similarity calculation.

## Overview

The vector space model consists of two main steps:

1. **Document Vectors Representation**: In this step, each document is broken down into words, and preprocessing techniques such as removing stopwords, punctuations, and special characters are applied. The documents are then represented as vectors of words.

2. **Term Document Matrix**: A term document matrix is constructed to represent document vectors in a matrix format. Each row represents term vectors across all documents, and each column represents document vectors across all terms. The cell values indicate the frequency counts of each term in the corresponding document.

## Term Weights Calculation

Once the term document matrix is created, term weights are calculated for all terms across all documents using the TF-IDF (Term Frequency-Inverse Document Frequency) formula:

- TF (Term Frequency): Number of times a term occurs in a document.
- IDF (Inverse Document Frequency): Inverse of the document frequency, calculated as log(N/df), where df is the document frequency (number of documents containing a term), and N is the total number of documents.

## Similarity Measures - Cosine Similarity

Cosine similarity is utilized to measure the similarity between document vectors and query vectors. It calculates the cosine angle between two vectors, representing their closeness. By calculating the cosine similarity between each document vector and the query vector, relevant documents to the query term can be identified. Documents with higher similarity scores are considered more relevant to the query.

## Key Components

1. **Document Representation**: Preprocess documents and represent them as vectors of words.
2. **Term Document Matrix**: Construct a term document matrix to represent document vectors.
3. **TF-IDF Calculation**: Calculate term weights using TF-IDF formula.
4. **Cosine Similarity**: Measure similarity between document vectors and query vectors using cosine similarity.

## Usage

- Preprocess documents and create a term document matrix.
- Calculate TF-IDF scores for terms in the matrix.
- Perform cosine similarity calculations between document vectors and query vectors.
- Retrieve relevant documents based on similarity scores.
