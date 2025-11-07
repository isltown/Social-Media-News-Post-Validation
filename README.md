# News Fact-Checking Pipeline

End-to-end workflow to **prepare a news dataset**, **train a LightGBM model**, and **run the complete fact-checking pipeline** that scores a social media post against a context article using TF–IDF/cosine features and gradient boosting.

## Repository structure

```

1) News Dataset Preparation.ipynb
2) Training LighGBM.ipynb
3) Complete Pipeline.ipynb
4) LightGBM Model File
5) TF-IDF Vectorizer File
6) Dataset
README.md
```

## What’s inside

### 1) News Dataset Preparation.ipynb
An executable notebook for building/cleaning the dataset and deriving text features ready for modeling.

### 2) Training LighGBM.ipynb
Trains a LightGBM classifier on engineered features (e.g., TF–IDF vectors and cosine similarities) and evaluates performance.

### 3) Complete Pipeline.ipynb
Stitches everything together: loads raw inputs (article + post), runs preprocessing/feature extraction, predicts with the trained model, and returns a final score/label.

## Getting started


### 1. Data
- Place the news/post data where the notebooks expect it (see the *Dataset Preparation* notebook cells for exact paths/filenames).
- Typical inputs:
  - **Context article**: title + full text
  - **Social post**: title/caption + body/text
- Extracted features:
  - TF–IDF representations
  - Cosine similarity measures between article and post fields

### 3. Running the notebooks
1. Open **News Dataset Preparation.ipynb**, run all cells to produce the processed dataset, the dataset has been provided in this repository as well.
2. Open **Training LighGBM.ipynb**, run all cells to train the model.
3. Open **Complete Pipeline.ipynb**, update paths to your model file and vectorizer and run to get predictions/scores for new (article, post) pairs.


