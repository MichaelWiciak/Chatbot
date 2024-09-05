# Chatbot Project

This project is a basic chatbot designed to interact with users by responding to various predefined queries about Giant Pandas. The chatbot is built using Python and utilizes Natural Language Processing (NLP) techniques with the help of libraries such as `nltk`, `tflearn`, and `tensorflow`.

## Project Overview

The chatbot is trained on a small dataset containing various user intents related to Giant Pandas, such as greetings, questions about panda behavior, habitat, and more. The chatbot processes user input, identifies the corresponding intent, and responds with a relevant answer from a predefined set of responses.

## Setup Instructions

### Prerequisites

Ensure you have the following installed:

- Python 3.x
- pip (Python package installer)

### Installation

1. Clone the repository or download the code files.

2. Install the required Python packages by running:

   ```bash
   pip install -r requirements.txt
   ```

   If you do not have a `requirements.txt` file, you can install the dependencies manually:

   ```bash
   pip install nltk tflearn tensorflow numpy
   ```

3. Download the NLTK data required for tokenization:

   ```python
   import nltk
   nltk.download('punkt')
   ```

4. Place the `intents.json` file in the same directory as `chatbot.py`.

## How It Works

1. **Data Loading**: The chatbot loads the `intents.json` file, which contains different user intents (e.g., greetings, questions about pandas) and their corresponding patterns and responses.

2. **Data Preprocessing**: The chatbot tokenizes the patterns in the intents using `nltk` and stems the words. It then creates a "bag of words" model, which is used to represent each pattern as a vector of binary values indicating the presence or absence of each word in the vocabulary.

3. **Model Training**: If the training data has not been preprocessed before, the chatbot creates training and output data by associating each pattern with its corresponding intent. This data is then used to train a neural network model using the `tflearn` library. The model is saved after training.

4. **Chat Interface**: The chatbot provides an interface where users can type their queries. The input is processed using the trained model to predict the intent, and the chatbot responds with a random response corresponding to that intent.

## Usage

To start the chatbot, run the following command in your terminal:

```bash
python chatbot.py
```

You will see a prompt where you can start interacting with the bot:

```
--------------------------------------------------------
Start talking with the bot (type quit to stop)!
You: 
```

Type your queries, and the bot will respond based on the trained intents. Type `quit` to exit the chat.

## Project Structure

- `chatbot.py`: The main Python script that runs the chatbot.
- `intents.json`: A JSON file containing the intents, patterns, and responses.
- `data.pickle`: A serialized file storing processed data (created after the first run).
- `model.tflearn`: The saved model file (created after training).

## Dependencies

- `nltk`: Natural Language Toolkit for tokenizing and stemming words.
- `tflearn`: A deep learning library that provides a high-level API for TensorFlow.
- `tensorflow`: An open-source library for machine learning.
- `numpy`: A library for numerical computations in Python.
- `json`: A library to handle JSON data.
- `pickle`: A library for serializing and deserializing Python objects.

