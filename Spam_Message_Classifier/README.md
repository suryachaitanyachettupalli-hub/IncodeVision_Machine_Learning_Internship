# Spam Message Classifier using NLP

**IncodeVision Machine Learning Internship — Task 03**

A beginner-friendly text classification project that uses TF-IDF and Logistic Regression to classify messages as spam or ham (not spam).

## Project features
- Loads and inspects the dataset with Pandas
- Checks missing values and removes exact duplicate rows
- Visualizes the ham/spam distribution
- Splits the dataset into training and testing sets with stratification
- Converts text into numerical features with TF-IDF
- Trains a Logistic Regression model using a Scikit-learn pipeline
- Evaluates with accuracy, precision, recall, F1-score, classification report, and confusion matrix
- Tests the model on new messages

## Files

```text
Task-03-Spam-Message-Classifier/
├── mail_data.csv
├── spam_message_classifier.ipynb
├── README.md
└── requirements.txt
```

## Requirements
- Python 3.10 or newer
- Jupyter Notebook

Install dependencies:

```bash
pip install -r requirements.txt
```

## How to run
1. Download or clone this folder.
2. Open a terminal in this folder.
3. Install the dependencies using the command above.
4. Start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

5. Open `spam_message_classifier.ipynb` and run the cells from top to bottom.

## Dataset note — please read
The provided `mail_data.csv` has two columns: `Category` (`ham` or `spam`) and `Message`. The messages appear SMS-like rather than full email bodies. This dataset is useful for learning spam text classification, but if the internship requirement is strictly **email spam detection**, replace it with a suitable email dataset and update this README before submitting.

## Evaluation
The notebook calculates test-set accuracy, spam precision, spam recall, spam F1-score, a classification report, and a confusion matrix. These values are calculated when the notebook is run; no performance score is guaranteed in advance.

## Technologies
- Python
- Pandas
- Matplotlib
- Scikit-learn
- TF-IDF
- Logistic Regression

## Learning outcomes
This project provides practice with data cleaning, exploratory analysis, text feature extraction, supervised classification, model evaluation, and making predictions on new text.
