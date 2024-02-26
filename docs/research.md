# GAIPAL Research Document

## *Members: Maxwell Malamut, Samantha Rigor, Jiasong Huang*

## Problem Understanding

GAIPAL is a living database that aims to become a valuable guiding resource for generative AI in various societal domains. Our team’s goal is to create a pipeline where users can input documents, and a LLM will extract relevant topics and keywords from these documents. Downstream visualization and analytic tasks can be built from the details extracted from documents. The topics crucial to further developing the GAIPAL web app are:

1. **Topic Extraction:** Users input documents, and the internal LLM must extract keywords and topics and the relevant sections containing these topics. The topics can either be preselected or generated from keywords the LLM finds. Document details can be stored for access later for search and analysis on the GAIPAL website.

2. **Data Preprocessing:** All documents require data preprocessing in order for the LLM to properly be able to digest the information. There are various methods of document preprocessing, but in general, it requires removing pictures and extraneous text from the document, leaving only the relevant information.

3. **Visualization:** After the documents have been processed, downstream tasks like topic models or semantic visualization graphs need to be built. Ideally, these visualizations will allow users to see how topics are related to documents as well as each other.

## Research Papers

### 1. A Topic Label Extraction Method for the University BBS

- **Summary:** Latent Dirichlet Allocation (LDA) is a statistical method for topic modeling that identifies underlying themes in a collection of documents by examining word and phrase distributions. It preprocesses data to remove redundancies and uses techniques like term frequency-inverse document frequency (TF-IDF) to extract significant keywords. The core of LDA involves determining the most probable topic for each word based on these keywords and adjusting topic weights through an artificial feedback mechanism to align with user requirements. This process not only helps in accurately categorizing documents into topics but also allows for dynamic adaptation to new data and user feedback, enhancing the model's relevance and accuracy over time.
- **Link:** [IEEE](https://ieeexplore.ieee.org/document/7866208)

### 2. Extracting Accurate Materials Data from Research Papers with Conversational Language Models and Prompt Engineering

- **Summary:** Conversational LLMs can be used to automate the selection of data from documents using prompt engineering. Initially, a simple relevancy prompt is employed to classify sentences, eliminating those without relevant data. In the second stage, sentences identified as relevant undergo further analysis for data extraction. Data is categorized based on whether it is single- or multi-valued, enabling more accurate extraction. Additionally, the possibility of missing data is explicitly acknowledged to prevent the generation of false information. Redundant prompts inducing uncertainty are utilized to prompt reanalysis when necessary, ensuring thorough analysis. All questions are embedded within a single conversation, leveraging conversational context to reinforce analysis. Lastly, a strict Yes/No format is enforced for answers, reducing uncertainty and facilitating automation throughout the process.
- **Link:** [arXiv](https://arxiv.org/abs/2303.05352)

### 3. Unsupervised Approaches for Automatic Keyword Extraction Using Meeting Transcripts

- **Summary:** While there has been extensive research on keyword extraction for written texts, there are fewer studies on the value of automatic keyword extraction for audio transcripts and automatic speech recognition (ASR). In this paper, the authors used term frequency-inverse document frequency (TF-IDF) weighting and graph-based approaches as models for unsupervised keyword extraction. Both methods were refined with other relevant factors, such as part-of-speech categories, word clusters, and sentence salience. The performance of these models was measured by comparison to human evaluations and F-measure scores. In both meeting transcripts and ASR, TF-IDF performed better than graph-based methods. Additionally, the additional restrictions (most prominently, sentence salience) on TF-IDF supported performance on transcripts, but they degraded performance on ASR keyword extraction. Despite the effectiveness of TF-IDF, though, both unsupervised models did not perform to the standards of human annotated keywords.
- **Link:** [ACL Anthology](https://aclanthology.org/N09-1070.pdf)

## Open Source

### h2ogpt

- **About:** h2ogpt uses open source LLMs from HuggingFace, ranging from models like LLaMa2, Mistral, and Falcon. These models are fed a pipeline with access to documents users submit and learn and retain information regarding these documents.
- **Links:** 
  - [h2ogpt GitHub](https://github.com/h2oai/h2ogpt)

### BERTopic

- **About:** BERTopic is a topic modeling technique that uses transformers to create clusters of information from text.
- **Links:** 
  - [BERTopic GitHub](https://github.com/MaartenGr/BERTopic)
