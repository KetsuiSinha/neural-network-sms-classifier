# SMS Spam Classifier

This project implements a machine learning model to classify SMS messages as either "ham" (normal messages) or "spam" (advertisements or promotional messages). The solution utilizes the SMS Spam Collection dataset, which is pre-split into training and testing data. The primary function, `predict_message`, takes a message string as input and outputs a prediction.

## Dataset
The dataset used is the **SMS Spam Collection dataset**, a well-known corpus for spam detection tasks. It contains labeled SMS messages categorized as either `ham` or `spam`.

## Objective
The goal is to create a function `predict_message` that:
- Accepts a single SMS message as input.
- Returns a list containing two elements:
  1. A float between 0 and 1 indicating the probability of the message being spam.
  2. A string: either `"ham"` or `"spam"` based on the prediction.

## Implementation Steps

1. **Data Preprocessing**:
   - Tokenize the text data.
   - Convert text to lowercase and remove unnecessary characters.
   - Use techniques like TF-IDF (Term Frequency-Inverse Document Frequency) for feature extraction.

2. **Model Selection**:
   - Train a machine learning model such as Naive Bayes, Logistic Regression, or Support Vector Machine.
   - Evaluate the model's performance on the test set using metrics like accuracy, precision, recall, and F1-score.

3. **Prediction Function**:
   - Define the `predict_message` function to preprocess the input text, predict probabilities, and output results in the desired format.

## Example Usage

```python
message = "Win a $1000 Walmart gift card now! Click here to claim."
prediction = predict_message(message)
print(prediction)  # Example output: [0.85, "spam"]
```

## Testing
The project includes test cases to validate the functionality of the `predict_message` function. Ensure your model is tested on the provided test dataset for reliable performance.
