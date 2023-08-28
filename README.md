# Sentiment Prediction Model with 7 Labels

## Overview
This repository contains a sentiment prediction model capable of classifying text into 7 distinct emotions: Angry, Curious, Disgusted, Fearful, Happy, Neutral, Sad, and Surprised. The model is designed to understand and categorize human emotions expressed in text data.

## Labels and Label IDs
- Angry (Label ID: 1)
- Curious (Label ID: 2)
- Disgusted (Label ID: 3)
- Fearful (Label ID: 4)
- Happy (Label ID: 5)
- Neutral (Label ID: 6)
- Sad (Label ID: 7)
- Surprised (Label ID: 8)

## Step-by-Step Approach

### 1. Data Collection and Preprocessing
- Gather a diverse dataset of text samples labeled with their corresponding sentiments.
- Preprocess the text data by tokenizing, removing stopwords, and converting to lowercase.

### 2. Initial Model with BERT
- Build an initial sentiment prediction model using the BERT (Bidirectional Encoder Representations from Transformers) architecture.
- Train the BERT model on the preprocessed dataset.
- Evaluate the model's accuracy on a validation set.

### 3. Transition to GBC Classifier
- Observe that the BERT model's accuracy is suboptimal for sentiment prediction.
- Decide to transition to a Gradient Boosting Classifier (GBC) for improved results.

### 4. Implement GBC Sentiment Classifier
- Create a GBCSentimentClassifier class to handle sentiment prediction using the Gradient Boosting Classifier.
- Train the GBC model on the preprocessed dataset, utilizing features extracted from the text data.

### 5. Model Performance Evaluation
- Compare the accuracy and performance of the GBC sentiment classifier with the initial BERT model.
- Notice a significant accuracy improvement with GBC.

### 6. Example Usage
- Provide sample code for using the GBC sentiment classifier in real-world scenarios.
- Highlight how AI chatbots can leverage the model to predict user sentiments and tailor responses accordingly.

## Approach
Initially, a sentiment prediction model was built using BERT (Bidirectional Encoder Representations from Transformers). However, the accuracy achieved was suboptimal, prompting a transition to a Gradient Boosting Classifier (GBC) for improved results.

## Model Performance
The shift to GBC significantly enhanced the accuracy and performance of the sentiment prediction model. This improvement holds immense potential, especially in AI chatbot applications. By predicting user sentiments, chatbots can tailor responses to match emotional nuances and enhance user experience.

## Example Usage
```python
from gbc_classifier import GBCSentimentClassifier

# Load the GBC sentiment classifier
classifier = GBCSentimentClassifier()

# Predict sentiment for a text
text = "Feeling excited about the upcoming project!"
predicted_sentiment = classifier.predict_sentiment(text)
print(f"Predicted sentiment: {predicted_sentiment}")

## Conclusion
This sentiment prediction model showcases the dynamic nature of AI in understanding and responding to human emotions. By combining accurate sentiment classification with AI chatbots, we can create more personalized and empathetic interactions, enhancing the overall user experience.

Feel free to customize and expand upon this README template to provide more specific details about your implementation, including code snippets and usage examples.
