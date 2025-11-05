# Spam Classifier (Email Spam Detection)

A simple machine learning project that detects spam messages using classic models and TF‑IDF features. This repository contains Jupyter notebooks exploring multiple algorithms on the same dataset.

## Contents
- `mail_data.csv`: Dataset of messages with labels
- `spam-detection.ipynb`: Baseline TF‑IDF + Logistic Regression
- `Spam-MultinomialNB.ipynb`: TF‑IDF + Multinomial Naive Bayes
- `spam-RandomForest.ipynb`: TF‑IDF + Random Forest

## Quickstart

### 1) Clone and set up environment
```bash
# Clone your new GitHub repo (after you push this project)
# git clone <your-repo-url>
# cd Spam Classifier

# Create and activate a virtual environment (recommended)
python -m venv .venv
# Windows PowerShell
. .venv\\Scripts\\Activate.ps1

# Install dependencies
pip install -r requirements.txt
```

### 2) Open notebooks
```bash
pip install jupyter
jupyter notebook
```
Open any of the notebooks and run cells top-to-bottom.

## Requirements
Dependencies are captured in `requirements.txt`. Detected from notebooks:
- numpy
- pandas
- scikit-learn
- nltk

If you see an error about NLTK resources (e.g., stopwords), download them inside a Python shell:
```python
import nltk
nltk.download('stopwords')
```

## Data
- File: `mail_data.csv`
- Ensure the file remains in the project root so notebooks can load it directly with pandas.

## Reproducing Results
1. Create/activate the virtual environment and install requirements
2. Launch Jupyter
3. Run:
   - `spam-detection.ipynb` for Logistic Regression
   - `Spam-MultinomialNB.ipynb` for MultinomialNB
   - `spam-RandomForest.ipynb` for Random Forest

Each notebook:
- Loads `mail_data.csv`
- Splits train/test
- Vectorizes text with TF‑IDF
- Trains the model
- Reports accuracy and common metrics

## Project Structure
```
Spam Classifier/
├─ mail_data.csv
├─ README.md
├─ requirements.txt
├─ .gitignore
├─ spam-detection.ipynb
├─ Spam-MultinomialNB.ipynb
└─ spam-RandomForest.ipynb
```

## How to Upload to GitHub
1. Create a new repo on GitHub (without initializing with README)
2. In this folder run:
```bash
git init
git add .
git commit -m "Initial commit: spam classifier notebooks"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
```
