# Sentiment Analysis of IMDB Movie Reviews

## Project Overview
This project focuses on **sentiment analysis** of movie reviews from the IMDB dataset. The model classifies movie reviews as either positive or negative, providing insights into audience feedback for movies. The task was implemented using an LSTM-based deep learning architecture to analyze the text data and predict sentiment.

## Dataset
The dataset used for this project contains **50,000 movie reviews** from the IMDB website, available on Kaggle: [IMDB Dataset of 50K Movie Reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews).

![The Dataset]([image_url](https://github.com/EngAhmed19/Sentiment_Analysis/blob/main/sentiment%20analysis/Images/Dataset.png))


### Data Preprocessing
To prepare the dataset, the following preprocessing steps were applied:
- Converted all text to **lowercase**.
- Removed **HTML tags** from reviews.
- Filtered out **non-alphabetic text**.
- Removed common **stop words** to focus on key terms.
- Applied **lemmatization** to reduce words to their root forms.
- Tokenized the reviews and applied **padding sequences** to ensure uniform input length.

![The Dataset after cleaning](https://github.com/EngAhmed19/Sentiment_Analysis/blob/main/sentiment%20analysis/Images/Dataset-after-cleaning.png)

The data was split into:
- **80% training data**
- **20% testing data**

## Model Architecture
The sentiment classification model is built using an **LSTM (Long Short-Term Memory)** architecture, known for its effectiveness with sequential data like text. Key details of the model include:
- **Embedding layer**: Converts text input into dense vectors of fixed size.
- **2 LSTM layers**: Used to capture the sequence information from the reviews.
- **Dropout layers**: Two dropout layers were added after each LSTM layer for **regularization** to prevent overfitting.
- **Softmax layer**: Outputs the probability distribution for positive and negative sentiment.

![The Archeticher](https://github.com/EngAhmed19/Sentiment_Analysis/blob/main/sentiment%20analysis/Images/The-model-Archecher.png)

### Training
- **Epochs**: 10
- **Batch Size**: 32
- **Optimizer**: Adam
- **Loss Function**: Sparse categorical cross-entropy

### Results
- **Training Accuracy**: 90%
- **Testing Accuracy**: 86%

## Gradio Interface
To make the model more interactive, a **Gradio GUI** was developed. This allows users to input a movie review and receive the predicted sentiment in real time.

![The Archeticher](https://github.com/EngAhmed19/Sentiment_Analysis/blob/main/sentiment%20analysis/Images/Gradio_Interface.png)
