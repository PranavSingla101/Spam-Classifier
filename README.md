# 📧 Spam Classifier

A machine learning project that detects spam emails using multiple classification algorithms. This repository contains Jupyter notebooks comparing different models (Logistic Regression, Multinomial Naive Bayes, and Random Forest) on the same email dataset using TF-IDF feature extraction.

## 🎯 Overview

This project implements and compares three different machine learning models for email spam detection:
- **Logistic Regression**: A linear classifier providing interpretable results
- **Multinomial Naive Bayes**: A probabilistic classifier well-suited for text classification
- **Random Forest**: An ensemble method using multiple decision trees

All models use **TF-IDF (Term Frequency-Inverse Document Frequency)** vectorization to convert text messages into numerical features.

## ✨ Features

- 📊 Comparison of three different ML algorithms
- 🔤 TF-IDF text vectorization for feature extraction
- 📈 Performance metrics and accuracy comparison
- 📓 Well-documented Jupyter notebooks
- 🔄 Reproducible experiments

## 📋 Table of Contents

- [Quick Start](#-quick-start)
- [Installation](#-installation)
- [Project Structure](#-project-structure)
- [Usage](#-usage)
- [Results](#-results)
- [Technologies Used](#-technologies-used)
- [Dataset](#-dataset)

## 🚀 Quick Start

### Prerequisites

- Python 3.7 or higher
- pip (Python package manager)

### Installation

1. **Clone the repository** (or download the project):
   ```bash
   git clone <your-repo-url>
   cd "Spam Classifier"
   ```

2. **Create a virtual environment** (recommended):
   ```bash
   # Create virtual environment
   python -m venv .venv
   
   # Activate virtual environment
   # Windows PowerShell:
   .\.venv\Scripts\Activate.ps1
   # Windows CMD:
   .venv\Scripts\activate.bat
   # macOS/Linux:
   source .venv/bin/activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Download NLTK data** (if needed):
   ```python
   import nltk
   nltk.download('stopwords')
   ```

5. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

## 📁 Project Structure

```
Spam Classifier/
├── mail_data.csv              # Email dataset (5572 messages)
├── README.md                  # Project documentation
├── requirements.txt           # Python dependencies
├── .gitignore                 # Git ignore file
├── spam-detection.ipynb       # Logistic Regression model
├── Spam-MultinomialNB.ipynb   # Multinomial Naive Bayes model
└── spam-RandomForest.ipynb    # Random Forest model
```

## 💻 Usage

Each notebook follows a similar workflow:

1. **Load the dataset** from `mail_data.csv`
2. **Preprocess** the text data
3. **Split** into training and testing sets
4. **Vectorize** text using TF-IDF
5. **Train** the model
6. **Evaluate** performance with accuracy and other metrics

### Running a specific model:

- **Logistic Regression**: Open and run `spam-detection.ipynb`
- **Multinomial Naive Bayes**: Open and run `Spam-MultinomialNB.ipynb`
- **Random Forest**: Open and run `spam-RandomForest.ipynb`

Each notebook can be run independently and will produce its own results.

## 📊 Results

### Model Performance Comparison

| Model                   | Train Accuracy | Test Accuracy |
|-------------------------|----------------|---------------|
| **Logistic Regression** | 96.77%         | 96.68%        |
| **Multinomial Naive Bayes** | 98.07%         | 97.31%        |
| **Random Forest**       | 100.00%        | 97.67%        |

### Key Observations

- ✅ **Random Forest** achieves the highest test accuracy (97.67%) but shows signs of overfitting with 100% training accuracy
- ✅ **Multinomial Naive Bayes** provides a good balance with 97.31% test accuracy and less overfitting
- ✅ **Logistic Regression** offers the most interpretable results with 96.68% test accuracy
- ✅ All models generalize well on the test set, demonstrating the effectiveness of TF-IDF features

## 🛠️ Technologies Used

- **Python 3**: Programming language
- **NumPy**: Numerical computing
- **Pandas**: Data manipulation and analysis
- **Scikit-learn**: Machine learning library
  - `TfidfVectorizer`: Text vectorization
  - `LogisticRegression`: Linear classifier
  - `MultinomialNB`: Naive Bayes classifier
  - `RandomForestClassifier`: Ensemble classifier
- **NLTK**: Natural language processing (stopwords)
- **Jupyter Notebook**: Interactive development environment

## 📦 Dependencies

All required packages are listed in `requirements.txt`:

```
numpy
pandas
scikit-learn
nltk
jupyter
```

## 📚 Dataset

- **File**: `mail_data.csv`
- **Size**: 5,572 email messages
- **Columns**:
  - `Category`: Label (ham/spam)
  - `Message`: Email text content
- **Location**: Keep the file in the project root directory for notebooks to load it correctly

## 🔄 Reproducing Results

To reproduce the results:

1. Ensure you have the dataset (`mail_data.csv`) in the project root
2. Install all dependencies from `requirements.txt`
3. Open any notebook in Jupyter
4. Run all cells sequentially (Cell → Run All)
5. Compare the accuracy metrics with the results table above

## 📝 Notes

- The dataset should remain in the project root directory
- NLTK stopwords may need to be downloaded on first run
- Results may vary slightly due to random train/test splits
- Random Forest's perfect training accuracy suggests potential overfitting

## 🤝 Contributing

Feel free to fork this project and experiment with:
- Different feature extraction methods (Word2Vec, GloVe, etc.)
- Additional models (SVM, XGBoost, etc.)
- Hyperparameter tuning
- Cross-validation strategies

## 📄 License

This project is open source and available for educational purposes.

---

**Happy Classifying! 🎉**
