# Amazon Customer Sentiment Analysis 📊🤖

An end-to-end Natural Language Processing (NLP) project built in Python to automatically analyze, clean, and classify the sentiment of Amazon product reviews.

## Project Overview
The goal of this project is to automate customer feedback analysis. By parsing raw text reviews, the system transforms unstructured human language into clean, mathematical inputs to accurately predict whether a customer's review is **Positive**, **Neutral**, or **Negative**. 

Automating this process allows companies to instantly flag unhappy customers and track sentiment trends at scale without needing human review teams to read every single line.

##  Tech Stack & Libraries Used
* **Python** (Core language)
* **Pandas** & **NumPy** (Data manipulation and structuring)
* **Matplotlib** & **Seaborn** (Exploratory Data Analysis and data visualization)
* **Scikit-Learn** (Feature extraction, train-test splitting, and model training)

## 📈 Key Steps Completed

### 1. Data Loading & Labeling
* Imported the **Amazon Fine Food Reviews** dataset using `kagglehub` directly into Google Colab.
* Managed computing limits by down-sampling the dataset to a balanced subset of 5,000 reviews.
* Engineered a custom sentiment labeling function mapping the 1-to-5 star ratings into categorical buckets:
  * 4–5 Stars ➡️ **Positive**
  * 3 Stars ➡️ **Neutral**
  * 1–2 Stars ➡️ **Negative**

### 2. Text Preprocessing (NLP Pipeline)
* Standardized text inputs by converting all strings to lowercase.
* Stripped out HTML tags, numerical values, special signs, and punctuation marks using regular expressions (`re`) to eliminate background noise.

### 3. Exploratory Data Analysis (EDA)
* Visualized the target column distribution using Seaborn count plots to understand class balance. 

### 4. Machine Learning & Feature Extraction
* Converted raw strings into a numerical vector grid using a **TF-IDF Vectorizer** tracking the top 2,500 most important words.
* Split the dataset into **80% Training** and **20% Testing** chunks.
* Trained a **Logistic Regression** classification model to evaluate incoming textual sentiment matrices.
* Generated comprehensive model performance report cards detailing Precision, Recall, and F1-Scores.

---

## 💡 Core Insights
* **Data Skew:** Like most commercial review datasets, the data is heavily skewed toward positive feedback. Knowing this skew is critical before deploying models to avoid biased predictions.
* **Automation Value:** Text preprocessing scales efficiently. Transforming text into TF-IDF frequencies provides highly interpretable data that linear models can read flawlessly to save hundreds of operational hours.
