# Semantic Search Engine

## Overview
This project implements a semantic search engine for a dataset of CNN news articles. The search engine utilizes Natural Language Processing (NLP) techniques to extract and rank news articles based on their relevance to a given query. The primary features of this project include tokenization, dictionary building, feature extraction using Bag of Words (BoW), and the use of Tf-Idf and Latent Semantic Indexing (LSI) models for improved search results.

## Key Features
This project includes the following key features:

1. **Tokenization**: The Spacy library is used to tokenize the CNN news dataset, breaking down the text into individual words or tokens.

2. **Building Word Dictionary**: The Gensim library is employed to create a dictionary of the corpus. This dictionary assigns unique IDs to each word and records their frequency counts. Additionally, it filters out words that occur in fewer than four articles or more than 20% of the articles, as these words are not likely to contribute meaningfully to the topics.

3. **Feature Extraction (Bag of Words)**: A Bag of Words (BoW) model is used to represent text as the occurrence of known words within a document. The `doc2bow` method in the Gensim dictionary is utilized to count the frequency of words in the corpus.

4. **Build Tf-Idf and LSI Model**: The Term frequency-Inverse Document Frequency (Tf-Idf) model is employed to determine the importance of words in each document. After building the Tf-Idf model, it is passed to the Latent Semantic Indexing (LSI) model, where you can specify the number of features to create.
   

6. **Semantic Search**: Users can input a search query, and the model will return relevant news articles along with a "Relevance %" score, which represents the similarity between the query and the documents. Higher similarity scores indicate greater relevance.


---

## TF-IDF (Term Frequency-Inverse Document Frequency) Model

TF-IDF is a critical part of our semantic search engine. It assigns importance to words in news articles based on their frequency in the document and rarity across the corpus. This benefits our project by:

- **Keyword Significance:** Identifying important words in articles.
- **Reducing Common Words:** Minimizing the impact of common terms.
- **Improved Ranking:** Enhancing search result quality.
- **Accurate Query Matching:** Helping users find relevant information.


---

## Latent Semantic Indexing (LSI) Model

The Latent Semantic Indexing (LSI) model is a crucial component of our semantic search engine project. It plays a pivotal role in enhancing the accuracy and effectiveness of the information retrieval process. In this section, we'll delve into what LSI is and how it has significantly benefited our project.

### Understanding Latent Semantic Indexing (LSI)

LSI is a mathematical technique used in natural language processing and information retrieval to uncover the hidden, or "latent," semantic structure in a corpus of text documents. The fundamental idea behind LSI is to represent the relationships between terms and documents in a way that captures their semantic meaning. This enables LSI to discover context and contextually related terms, ultimately improving the quality of search results.

### Key Benefits in Our Project

1. **Semantic Understanding:** LSI provides a higher-level understanding of the content within news articles. It is not solely based on the frequency of words but takes into account the contextual relationships between words. This means that LSI can recognize the similarity between documents that may not share many common words but are related in meaning. 

2. **Reducing Noise:** LSI helps in reducing the noise in the dataset by capturing the underlying semantics. It mitigates the impact of synonyms, polysemy (words with multiple meanings), and noisy terms that can affect the quality of search results. 

3. **Improved Relevance Scoring:** LSI enhances the calculation of the "Relevance %" score for search results. By considering the semantic context, the search engine can better match user queries with the content of news articles, providing more accurate and contextually relevant scores.

4. **Improved Query Expansion:** LSI aids in query expansion by suggesting related terms that might not be present in the original query. This enables users to discover relevant articles even when they use different terminology.

5. **Handling Ambiguity:** LSI helps disambiguate terms with multiple meanings. It can distinguish between different senses of a word based on the context in which it appears, thereby reducing ambiguity in search results.

In summary, the LSI model is a fundamental component of our semantic search engine. It goes beyond simple keyword matching and considers the underlying semantics of the content, resulting in more accurate and contextually relevant search results. This enhancement significantly benefits the project by improving the quality of information retrieval and making it a more powerful and effective tool for searching CNN news articles.

---

## Getting Started
### Prerequisites
Before using this project, ensure you have the following prerequisites installed:

- Python (>=3.6)
- Spacy
- Gensim
- Pandas
- Other dependencies (refer to the requirements.txt file)

   ```
## Usage
### Data Preprocessing
1. Tokenization: Tokenize the CNN news dataset using the Spacy library.
2. Build Word Dictionary: Create a dictionary of the corpus with unique word IDs and frequency counts. Filter out less relevant words.

### Semantic Search
1. Build Tf-Idf and LSI Model: Generate Tf-Idf models to determine word importance in each document, and pass them to the LSI model to create semantic features.

2. Time for Semantic Search: Input a search query, and the model will return relevant news articles along with a "Relevance %" score, indicating their similarity to the query.

## Results
The project returns search results based on semantic relevance, allowing users to quickly find relevant CNN news articles. The "Relevance %" score provides a measure of how closely the articles match the search query.

