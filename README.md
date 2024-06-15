# ToxiDetect: AI-Powered Toxic Comment Detection

## Overview

ToxiDetect is an AI-powered model designed to identify and classify toxic comments using advanced deep learning techniques. Leveraging TensorFlow and Bidirectional LSTMs, this model detects various types of toxicity in comments, including insults, threats, profanity, hate speech, harassment, and more.

## Features

- **Deep Learning Model**: Utilizes Bidirectional LSTM with Embedding layers for text processing.
- **Comprehensive Toxicity Detection**: Classifies comments into six categories of toxicity.
- **Interactive Interface**: Gradio-based web app for real-time comment scoring.
- **High Performance**: Trained on a large dataset for accurate and reliable detection.

## Installation

1. **Clone the repository:**
   ```sh
   git clone https://github.com/StrangeCoder1729/ToxiDetect.git
   cd ToxiDetect
   ```

2. **Mount Google Drive (if using Google Colab):**
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

## Usage

1. **Load the Dataset:**
   ```python
   df = pd.read_csv('/content/drive/My Drive/YOUTUBE/Deep_Learning/Toxic_Comments/train.csv/train.csv')
   ```

2. **Preprocess the Data:**
   ```python
   vectorizer.adapt(X.values)
   ```

3. **Train the Model:**
   ```python
   history = model.fit(train, epochs=1, validation_data=val)
   ```

4. **Evaluate the Model:**
   ```python
   precision = Precision()
   recall = Recall()
   accuracy = CategoricalAccuracy()
   # ... (evaluation code)
   ```

5. **Run the Gradio Interface:**
   ```python
   interface.launch(share=True)
   ```

## Model Prediction

To make predictions on new comments:
```python
input_txt = vectorizer('Your comment here')
result = model.predict(np.expand_dims(input_txt, 0))
```

## Example

Test the model with a sample comment:
```python
result = score_comment("You are an idiot!")
print(result)
```

## Gradio App

Launch the interactive Gradio app to score comments in real-time:
```python
interface.launch(share=True)
```

## Credits

- **Nicholas Renotte**: [GitHub Profile](https://github.com/nicknochnack)

 
