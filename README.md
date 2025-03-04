# Key Phrase Extraction and Analysis

## Overview
This project analyzes the terminologies used in the collected corpus and identifies key trends in the study domain. By extracting key phrases and training Word2Vec embeddings, we aim to understand the evolving vocabulary and relationships between terms. 

Additionally, we perform exact phrase matching against a predefined trait phrase dictionary to gain extra insights into overlap between extracted terms and existing knowledge.

## Workflow
1. **Data Preprocessing**
   - Lowercasing, punctuation removal, tokenization, stop words removal, and lemmatization.
2. **Key Phrase Extraction**
   - Uses RAKE, TF-IDF, and n-gram modeling to identify key phrases.
3. **Word2Vec Training**
   - Trains a Word2Vec model on the corpus to learn word associations.
   - Generates word embeddings to analyze related terms and emerging terminology.
4. **Phrase Matching**
   - Compares extracted phrases to known trait phrases.
   - Computes coverage and exact match percentages.
5. **Evaluation Metrics**
   - **Key Terminology Trends:** Identify frequently occurring and emerging terms.
   - **Word2Vec Similarity:** Cluster similar concepts and analyze contextual word relationships.
   - **Coverage (%):** Extracted phrases as a percentage of trait phrases.
   - **Exact Match (%):** Percentage of extracted phrases that exactly match trait phrases.

## Results Interpretation
- **High Frequency in Key Phrases & Word2Vec Similarity** → Indicates dominant research trends.
- **Newly Emerging Phrases** → Suggests evolving focus in the study domain.

## Word2Vec Model Training
To understand the relationships between terms, we train a **Word2Vec model** using the extracted phrases. This helps in:
- **Identifying semantically related words** (e.g., "genomics" → "genetic_variation").
- **Analyzing how terms cluster together** in the research domain.
- **Detecting terminology evolution over time**.

## Future Improvements
- Integrate BERT embeddings for more robust terminology analysis.
- Use topic modeling (LDA, BERTopic) to uncover hidden themes in the corpus.
- Fine-tune stopword handling and phrase scoring thresholds.
- Explore other key phrase extractors

## Report & Analysis
For a detailed report on findings and term analysis, refer to:
[Phrase Mining Report (PDF)](report/Phrase%20Mining%20Report.pdf). 

## Dependencies
- `scikit-learn`
- `nltk`
- `gensim`
- `rake-nltk`
- `pandas`