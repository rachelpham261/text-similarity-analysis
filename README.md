# Text Mining Project: Document Similarity & Text Analysis

This project focuses on analyzing two literary works to compare their content and style. The analysis includes text cleaning, exploration, feature engineering, vectorization, and comparison to derive insights into the themes, vocabulary, and narrative styles of the texts.

## Dependencies

- Python 3.x
- NLTK (Natural Language Toolkit)
- scikit-learn
- WordCloud
- Matplotlib

## Setup

1. **Installation**: Ensure Python 3.x is installed on your system. Install the required Python packages using pip:

```bash
pip install nltk scikit-learn matplotlib wordcloud
```

2. **NLTK Data**: Download the necessary NLTK datasets:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('averaged_perceptron_tagger')
```

## Files

- **`document_similarity.ipynb`**: The main notebook containing all the code for the project.
- **`pandp.txt`** and **`sands.txt`**: Text files containing the literary works to be analyzed. Note that the notebook works for any pair of documents.
- **`report.pdf`**: The project report.

## Usage

1. Ensure all dependencies are installed and NLTK data is downloaded.
2. Place the text files in the same directory as the `document_similarity.ipynb`.
3. Run the cells in `document_similarity.ipynb` sequentially.
4. The notebook will output the results of the analysis, including Word Clouds, Dispersion Plots, and the cosine similarity scores.

## Workflow

### 1. Text Cleaning

The first step involves preparing the text data by:
- Extracting the main content from additional metadata.
- Removing extra white spaces and non-alphabet characters.
- Converting all characters to lowercase.
- Removing stopwords.

### 2. Tokenization

We use NLTK's word tokenizer to break down the text into individual words (tokens).

### 3. Exploration

This phase includes creating Word Clouds and Dispersion Plots to visually explore the dominant words and their distribution in the documents, respectively.

### 4. Feature Engineering

We consider 2 feature engineering tasks for each document:

1. POS tagging followed by Lemmatization
2. N-grams

Each document will have 2 sets of features corresponding to 2 feature engineering tasks.

### 5. Vectorization

Using TF-IDF (Term Frequency-Inverse Document Frequency), we vectorize the features generated in the previous step to numerically represent our text data.

### 6. Comparison

We calculate the cosine similarity between the documents using both sets of features to understand their similarity in terms of content and style.