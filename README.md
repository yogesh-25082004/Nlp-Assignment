"# Nlp-Assignment" 

OUTPUT IS IN THE LAST

















Sentiment Analysis + QoS Deep Learning Model
============================================

Overview
--------
This project combines **YouTube comments sentiment analysis** with **Quality of Service (QoS) metrics** to train a deep neural network for multi-class classification (Positive, Neutral, Negative sentiment).


Technologies Used:
- pandas & numpy
- Hugging Face Transformers (BERT sentiment analysis)
- PyTorch (for model training)
- scikit-learn (StandardScaler)

Dataset:
--------
- **Source:** Local CSV file (`YoutubeCommentsDataSet.csv`).
- Expected columns: One of the columns should be named `Comment` (adjust if needed).

How It Works:
-------------
1. **Load Dataset:** Reads a CSV file of YouTube comments.
2. **Clean Text:** Removes URLs, special characters, and converts text to lowercase.
3. **Sentiment Labeling:** Uses Hugging Face’s `sentiment-analysis` pipeline to classify comments and maps them into:
   - `0`: Negative
   - `1`: Neutral
   - `2`: Positive
4. **QoS Simulation:** Randomly generates 4 features:
   - Bitrate
   - Buffering
   - Resolution
   - Viewers
5. **Training:** Combines QoS features with sentiment scores and trains a deep neural network (multi-class classification using CrossEntropyLoss).
6. **Prediction:** New comments are cleaned, passed through BERT for sentiment scoring, QoS is simulated, and the model predicts the final sentiment.
