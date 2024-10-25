# Fake News Prediction Model  
This project implements a **Fake News Prediction Model** using **Logistic Regression**. The goal is to classify news articles as either **real** or **fake**. This is a basic **binary classification task**.

---

## Overview  
With the increasing spread of misinformation, this model aims to detect **fake news** using **machine learning techniques**. It leverages text preprocessing methods such as **stemming** and **vectorization** to prepare the data for model training. The model uses a **logistic regression algorithm**, which is suitable for binary classification.

---

## Dataset Description  
The dataset used for this project is from Kaggle: [Fake News Dataset](https://www.kaggle.com/c/fake-news/data?select=train.csv). It contains both **real and fake news articles**, which have been labeled accordingly. 

### Features:  
- **id:** unique id for a news article  
- **title:** he title of a news article
- **author:** author of the news article 
- **text:** the text of the article; could be incomplete
- **label:** a label that marks the article as potentially unreliable (0 = Real, 1 = Fake)

---

## Model Performance  
The model performed well on both the **training set** and **testing set**, achieving the following accuracy:

- **Training Accuracy:** 98.64%  
- **Testing Accuracy:** 97.91%

Due to time constraint the model was only trained on an attrbute combination of 'author' and 'title' rather than 'text'
---

## Usage  
Here’s how to use the model to predict whether a given news article is real or fake:

```python
# Example usage with test data
X_new = X_test[1]  # Select a news article from the test set

# Predict whether the news is real or fake
prediction = model.predict(X_new)

# Print the result
if prediction == 1:
    print('THIS NEWS IS FAKE!')
else:
    print('THIS NEWS IS REAL!')
