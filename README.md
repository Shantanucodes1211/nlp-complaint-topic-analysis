# DLBDSEDA02 - NLP-Based Complaint Topic Analysis

## Author

Shantanu Taralekar

## Project Overview

This project was developed for the IU course **Project: Data Analysis (DLBDSEDA02)**.  
The selected portfolio task is **Task 1: Use NLP techniques to analyze a collection of texts**.

The objective of this project is to analyze complaint texts using Natural Language Processing techniques. The project identifies recurring topics from unstructured complaint narratives and presents them in a structured format. The implementation follows the Phase 1 concept by applying text preprocessing, vectorization, and topic modelling techniques.

## Dataset

The project uses the **Consumer Complaint Database** dataset from Kaggle.  
The dataset contains complaint records related to financial products and services. For this analysis, the column **Consumer complaint narrative** is used because it contains the written complaint text.

The full dataset file `complaints.csv` is not uploaded to this repository because of file size considerations. To run the notebook, the dataset should be downloaded separately from Kaggle and placed in the required Google Drive folder.

## Methodology

The analysis follows these steps:

1. Load the complaint dataset.
2. Inspect the dataset structure.
3. Select the complaint narrative column.
4. Remove missing and duplicate complaint texts.
5. Clean and preprocess the text.
6. Convert the cleaned text into numerical vectors using:
   - Bag of Words
   - TF-IDF
7. Extract prevalent topics using:
   - Latent Dirichlet Allocation
   - Non-negative Matrix Factorization
8. Compare the vectorization and topic modelling methods.
9. Save topic modelling outputs as CSV files.

## Text Preprocessing

The preprocessing step includes:

- Lowercase conversion
- URL removal
- Number removal
- Punctuation removal
- Special character removal
- Stopword removal
- Dataset-specific custom stopword removal
- Removal of redacted terms such as `XXXX`
- Lemmatization

These steps reduce noise in the complaint narratives and improve the quality of vectorization and topic modelling.

## Vectorization Methods

Two vectorization methods are applied:

1. **Bag of Words**  
   This method converts complaint texts into word-frequency counts. It is used as input for LDA.

2. **TF-IDF**  
   This method measures word importance by considering both word frequency and rarity across documents. It is used as input for NMF.

## Topic Modelling Methods

Two topic modelling techniques are applied:

1. **Latent Dirichlet Allocation**  
   LDA is used to identify probabilistic topic groups from the Bag of Words matrix.

2. **Non-negative Matrix Factorization**  
   NMF is used to extract interpretable topic groups from the TF-IDF matrix.

## Technologies Used

- Python
- Google Colab
- pandas
- NumPy
- NLTK
- scikit-learn
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

1. Download the Consumer Complaint Database dataset from Kaggle.
2. Rename the dataset CSV file to `complaints.csv`.
3. Place `complaints.csv` inside the Google Drive folder used in the notebook.
4. Open `nlp_complaint_topic_analysis.ipynb` in Google Colab.
5. Mount Google Drive.
6. Run all notebook cells from top to bottom.
7. Review the generated LDA and NMF topic modelling results.

## Repository Structure

```text
DLBDSEDA02-nlp-complaint-analysis/
│
├── nlp_complaint_topic_analysis.ipynb
├── README.md
├── requirements.txt
├── lda_topics.csv
├── nmf_topics.csv
├── vectorization_comparison.csv
└── model_comparison.csv
