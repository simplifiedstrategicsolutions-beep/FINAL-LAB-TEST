# Emotion Detection Web App

A Flask web application that analyzes customer feedback text and identifies the emotion it expresses. It returns scores for **anger, disgust, fear, joy, and sadness**, plus the **dominant emotion**, using the Watson NLP EmotionPredict service.

## Project Structure

```
oaqjp-final-project-emb-ai/
├── EmotionDetection/
│   ├── __init__.py
│   └── emotion_detection.py
├── static/
│   └── mywebscript.js
├── templates/
│   └── index.html
├── server.py
├── test_emotion_detection.py
└── README.md
```

## Requirements

- Python 3
- `requests`
- `flask`

```bash
python3 -m pip install requests flask
```

## Usage

### Run the web app

```bash
python3 server.py
```

Open the app on port 5000, enter a statement, and click **Run Emotion Detection**. Blank input returns `Invalid text! Please try again!`

### Use the function directly

```python
from EmotionDetection.emotion_detection import emotion_detector

print(emotion_detector("I love this new technology"))
```

The function returns a dictionary with the five emotion scores and a `dominant_emotion` key.

## Running the Tests

```bash
python3 -m unittest -v test_emotion_detection.py
```

The tests check that each of five sample statements produces the expected dominant emotion (joy, anger, disgust, sadness, fear).

## Static Code Analysis

```bash
python3 -m pip install pylint
pylint server.py
```

## Note

The Watson endpoint is typically reachable only from within the IBM Skills Network lab environment.

## Author

Your Name
