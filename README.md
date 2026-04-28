# DLBDSEDA02 - NLP-Based Complaint Topic Analysis

## Project Overview

This project was developed for the IU course **Project: Data Analysis (DLBDSEDA02)**.  
The selected portfolio task is **Task 1: Use NLP techniques to analyze a collection of texts**.

The objective of this project is to analyze complaint texts using Natural Language Processing techniques. The project identifies recurring topics from unstructured complaint narratives and presents them in a structured format.

## Dataset

The project uses the **Consumer Complaint Database** dataset from Kaggle.  
The dataset contains complaint records related to financial products and services.  
For this analysis, the column **Consumer complaint narrative** is used because it contains the written complaint text.

## Methodology

The analysis follows these steps:

1. Load the complaint dataset.
2. Select the complaint narrative column.
3. Remove missing and duplicate complaint texts.
4. Clean and preprocess the text.
5. Convert text into numerical vectors using:
   - Bag of Words
   - TF-IDF
6. Extract prevalent topics using:
   - Latent Dirichlet Allocation
   - Non-negative Matrix Factorization
7. Compare the results.
8. Save topic modelling outputs as CSV files.

## Text Preprocessing

The preprocessing step includes:

- Lowercase conversion
- URL removal
- Number removal
- Punctuation removal
- Special character removal
- Stopword removal
- Lemmatization

## Technologies Used

- Python
- Google Colab
- pandas
- NumPy
- NLTK
- scikit-learn
- gensim
- matplotlib
- wordcloud

## Output Files

The notebook generates the following output files:

- `lda_topics.csv`
- `nmf_topics.csv`
- `vectorization_comparison.csv`
- `model_comparison.csv`
- `requirements.txt`

## How to Run

1. Open `nlp_complaint_topic_analysis.ipynb` in Google Colab.
2. Mount Google Drive.
3. Place `complaints.csv` inside the selected Google Drive folder.
4. Run all notebook cells from top to bottom.
5. Review the generated topic modelling results.

## Author

Shantanu Taralekar