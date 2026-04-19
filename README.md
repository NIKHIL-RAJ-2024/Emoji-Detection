# Emoji Detection

A Streamlit web app that predicts the emotion of input text and displays an emoji with class probabilities.

## Features

- Text emotion prediction using a pre-trained scikit-learn pipeline.
- Emoji mapping for predicted emotion labels.
- Probability bar chart visualization using Altair.
- Compatible model loading from either `model/text_emotion.pkl` or `text_emotion.pkl`.

## Project Structure

```text
Emoji-Detection/
	app.py
	emotion_dataset_raw.csv
	text_emotion.pkl
	README.md
```

## Tech Stack

- Python 3.12+
- Streamlit
- pandas
- numpy
- altair
- joblib
- scikit-learn

## Quick Start

1. Clone the repository:

```bash
git clone https://github.com/NIKHIL-RAJ-2024/Emoji-Detection.git
cd Emoji-Detection
```

2. Create a virtual environment inside the project:

```bash
python3 -m venv .venv
```

3. Activate it:

```bash
source .venv/bin/activate
```

4. Install dependencies:

```bash
pip install --upgrade pip
pip install streamlit pandas numpy altair joblib scikit-learn
```

5. Run the app:

```bash
streamlit run app.py
```

## Usage

1. Enter any sentence in the text box.
2. Click Submit.
3. View predicted emotion, emoji, confidence score, and probability chart.

## Model Notes

- The model file expected by the app is `text_emotion.pkl` (or `model/text_emotion.pkl` if you choose to organize it in a folder).
- If you retrain and save a new model, keep the same filename or update `app.py` accordingly.

## Troubleshooting

### FileNotFoundError for model path

Cause:
The app cannot find the model file.

Fix:
- Ensure one of these files exists:
- `text_emotion.pkl`
- `model/text_emotion.pkl`

### Streamlit not found

Cause:
Dependencies are not installed in the active environment.

Fix:
```bash
source .venv/bin/activate
pip install streamlit pandas numpy altair joblib scikit-learn
```

### scikit-learn InconsistentVersionWarning

Cause:
The pickle was trained with a different scikit-learn version.

Fix options:
- Use the warning as-is for local testing if predictions look reasonable.
- Retrain and re-save the model using your current scikit-learn version for production reliability.

## Git Ignore

The repository includes `.gitignore` to exclude virtual environments, cache files, and local editor artifacts.

## License

No license file is currently defined. Add a `LICENSE` file if you plan to distribute this project.
