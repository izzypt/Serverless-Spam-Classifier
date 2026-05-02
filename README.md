# Serverless-Spam-Classifier

End-to-end serverless spam classifier, combining Scikit-learn for model development with AWS Lambda, Amazon S3, and Amazon API Gateway for deployment

This project demonstrates how to bridge the gap between machine learning experimentation and real-world deployment.

# 1. Prerequisites

 - **Fundamental skills**:
   - Basic proficiency in Python and understanding of Machine Learning concepts like classification.

- **AWS account**:
  - Access to an AWS account with permissions for Lambda, S3, and API Gateway.

- **Environment**:
  - Python 3.11 installed, along with libraries like scikit-learn, pandas, and joblib.

- **AWS CLI**:
  - Configured on your local machine for file uploads.

- **HuggingFace account**:
  - You can directly download the model.

# 2. Building the Brain: The Model

<img width="1000" height="563" alt="image" src="https://github.com/user-attachments/assets/6bb9bdbf-5bda-4540-aff6-82a292bdf04a" />


At the heart of this project lies a supervised learning approach. 

Instead of simply specifying which words are considered spam, we'll provide the computer with a dataset and an algorithm, enabling it to learn and identify spam patterns on its own.





### 1. Vectorization: Turning Text into Math
 
 Machine Learning models can't read text. They require numerical input. To solve this, we used the TF-IDF (Term Frequency-Inverse Document Frequency) Vectorizer. Read more about it here :

 - https://www.freecodecamp.org/news/how-to-extract-keywords-from-text-with-tf-idf-and-pythons-scikit-learn-b2a0f3d7e667/

 ```py
 feature_extraction = TfidfVectorizer(min_df=1, stop_words='english', lowercase=True)
  X_train_features = feature_extraction.fit_transform(X_train
```
