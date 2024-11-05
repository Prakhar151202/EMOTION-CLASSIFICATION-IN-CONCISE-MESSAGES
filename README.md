# Emotion Classification in Short Text

This project focuses on classifying short text messages into five emotion categories: joy, sadness, anger, fear, and neutral. It explores various text classification techniques, including traditional machine learning, deep learning, and transfer learning with BERT.

## Datasets

**Overview of Datasets Used:**

| Dataset          | Year | Type          | Size         | Emotion Categories                    | Balanced |
|------------------|------|---------------|--------------|---------------------------------------|----------|
| DailyDialog      | 2017 | Dialogues     | 102k samples | neutral, joy, surprise, sadness, anger, disgust, fear | No       |
| Emotion-Stimulus | 2015 | Dialogues     | 2.5k samples | sadness, joy, anger, fear, surprise, disgust | No       |
| ISEAR            | 1990 | Situations    | 7.5k samples | joy, fear, anger, sadness, disgust, shame, guilt | Yes      |

Links: [DailyDialog](http://yanran.li/dailydialog.html), [Emotion-Stimulus](http://www.site.uottawa.ca/~diana/resources/emotion_stimulus_data), [ISEAR](http://www.affective-sciences.org/index.php/download_file/view/395/296/)

### Combined Dataset
We combined and simplified these datasets to create a balanced set with 5 emotion categories: joy, sad, anger, fear, and neutral. The dataset mainly includes short messages and dialogue excerpts.

## Experiments

### 1. Traditional Machine Learning
- **Preprocessing**: Removed noise and punctuation, tokenized, and stemmed the text.
- **Text Representation**: Used TF-IDF to encode word importance.
- **Models**: Naive Bayes, Random Forest, Logistic Regression, and SVM.

| Model              | F1-Score |
|--------------------|----------|
| Naive Bayes        | 0.6702   |
| Random Forest      | 0.6372   |
| Logistic Regression| 0.6935   | 
| SVM                | 0.7271   | 

### 2. Neural Networks
- **Preprocessing**: Removed noise and punctuation, tokenized.
- **Word Embeddings**: Used pretrained Word2Vec (300 dimensions).
- **Models**: LSTM, BiLSTM, CNN.

| Model               | F1-Score |
|---------------------|----------|
| LSTM + Word2Vec     | 0.7395   |
| BiLSTM + Word2Vec   | 0.7414   |
| CNN + Word2Vec      | 0.7580   |

### 3. Transfer Learning with BERT
- **Model**: Fine-tuned BERT for emotion classification.
  
| Model              | F1-Score |
|--------------------|----------|
| Fine-tuned BERT    | 0.8320   |
