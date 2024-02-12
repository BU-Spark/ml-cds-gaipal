# Technical Project Document

## *Maxwell Malamut, Sam Rigor, Jiasong Huang, 2024-02-12 v0.0.1-dev*

## Overview


### A. Provide a solution in terms of human actions to confirm if the task is within the scope of automation through AI.

 - Redo analysis of documents on higher education by reading articles and adding summaries and keywords associated with these articles.
 - Source different types of documents to add to the database and analyse them as well.
 - Once all documents have summaries and keywords, group articles with similar topics and keywords into document groups so that upon keyword search, the relevent documents appear.


### B. Problem Statement:

 - A topic modeling, NLP, and network analysis pipeline to parse documents relevant to generative AI such that users can add documents, have their keywords and topics extracted, and search for specific documents with a given topic using topic modeling.


### C. Checklist for project completion

1. ML Pipeline: 
* Parse input document using NLP and topic modeling to extract keywords and topics. 
* Use network analysis in such a way that users can find similar and relevant topics easily. 
* Using NLP summarize documents in a concise and useful way.
2. Data Pipeline:
* Data cleaning in such a way that text, image, and links can all be parsed through the ML pipeline without causing issues.
* Normalize data by removing stop words and clutter from the actual document.
3. Proof-of-concept:
* Create a data pipeline to train the ML model given the documents we have.
* Allow for users to add documents to the document pool.
* Add searching and visualization for the extracted document data.
* Compare topic visualization from ML pipeline with previously annotated documents to judge topic modeling quality.

### D. Outline a path to operationalization.

 - Utilizing the previously existing webapp, integrate the data cleaning and machine learning pipelines. The end goal is to have a user simply upload a document they would like to have analysed and added to the document pool, and have the ML pipeline provide useful details about the topics contained in the document, as well as documents with similar topics.
 - Users will be able to show a topic word cloud and see which documents contain specfic topics and how topics are interconnected.
 - Tools: python visualization tools (matplotlib, seaborne, wordcloud), document processing tools (pandas), deep learning (pytorch, keras, tensorflow, HF transformers, BERTopic)

## Resources

### Data Sets

- Data previously provided by GAIPAL

### References

1. https://huggingface.co/docs/hub/en/bertopic

## Weekly Meeting Updates

*Keep track of ongoing meetings in the Project Description document prepared by Spark staff for your project.*


Note: Once this markdown is finalized and merge, the contents of this should also be appended to the Project Description document.