# sentiment_analysis
This project implements a sentiment classifier for tweets using classical machine learning techniques from scikit-learn.
The goal is to classify whether a tweet expresses emotion toward a brand or product and improve validation accuracy beyond the baseline.

🚀 Project Overview

Task: Binary sentiment classification on tweet text

Dataset: tweets.csv

Model: Naive Bayes (MultinomialNB)

Feature Extraction: Bag-of-Words (CountVectorizer)

Tracking: Weights & Biases (wandb)

Baseline Validation Accuracy: ~66%

Target Accuracy: ≥ 68%
Dataset Description (tweets.csv)

The dataset consists of tweets labeled for emotional intent.

Important Columns

tweet_text

Raw tweet content (text)

is_there_an_emotion_directed_at_a_brand_or_product

Target label indicating sentiment/emotion

Rows with missing tweet text are automatically removed during preprocessing.
Methodology
1️⃣ Data Loading & Cleaning

Loaded using Pandas

Null tweet entries are filtered out

2️⃣ Feature Extraction

CountVectorizer

Converts text into word frequency vectors

Vocabulary learned from entire dataset

CountVectorizer()

3️⃣ Model Training

Multinomial Naive Bayes

First 6000 tweets used for training

MultinomialNB()

4️⃣ Evaluation

Remaining tweets (6000–9091) used for validation

Accuracy computed for:

Training set

Validation set

 Experiment Tracking

This project uses Weights & Biases to log metrics:

Training Accuracy

Validation Accuracy

wandb.log({
  "train_accuracy": train_accuracy,
  "val_accuracy": val_accuracy
})


Make sure you are logged into W&B before running the script.

 Installation & Setup
1️ Clone the Repository
git clone https://github.com/your-username/tweet-sentiment-classifier.git
cd tweet-sentiment-classifier

2️ Install Dependencies
pip install pandas numpy scikit-learn wandb

3️ Login to Weights & Biases
wandb login

4 Running the Project
python sentiment.py


After execution:

Accuracy metrics will be printed

Results will be logged to your W&B dashboard

 Possible Improvements (Next Steps)
