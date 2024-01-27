# PsychometricTester-and-Analyzer


Project Overview
This project integrates computational linguistics with machine learning to predict Myers-Briggs Personality Types based on Twitter data. Utilizing the extensive Myers-Briggs Personality Type Dataset, which comprises over 8600 entries of individual MBTI types and their corresponding social media posts, our model offers insightful personality analyses.

Data Acquisition and Preprocessing
Data Source: We leverage the Myers-Briggs dataset, where each record contains a user's MBTI type and a compilation of their last 50 posts, separated by "|||".
Twitter Integration: Using Tweepy and the Twitter API, we fetch a user's 50 latest tweets based on their username. These tweets are stored in a CSV file for processing.
Preprocessing Steps: We employ regex to filter out special characters and emojis. The posts are then cleaned to remove stopwords, punctuation, and are converted to lowercase. Stemming techniques are applied to distill words to their root forms. This cleaned data is then divided using a train-test split.

Model Development
LSTM Model: Our baseline model uses Long Short-Term Memory (LSTM) networks, a type of Recurrent Neural Network (RNN) well-suited for handling long-term dependencies. LSTMs efficiently manage increasing error gradients and weights, outperforming traditional RNNs.
TensorFlow and Keras: TensorFlow provides the backbone for creating extensive neural networks, and Keras, a high-level library built on TensorFlow, offers a user-friendly interface for rapid prototyping of these networks.
BERT Integration: We enhance our model's accuracy by incorporating BERT (Bidirectional Encoder Representations from Transformers), a Google-developed technique for NLP pre-training. BERT effectively computes vector-space representations of language, integrating seamlessly into our deep learning model.

Prediction and UI Interaction
Model Prediction: The cleaned data is fed into both the LSTM and BERT base uncased models for personality prediction.
User Interface: Initial results are briefly displayed on the screen. Users can then navigate to a detailed dashboard to explore an in-depth analysis of their personality type, based on their Twitter activity.
