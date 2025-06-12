# MindMateAI - Your Wellness Companion Chatbot
 
An intelligent mental wellness assistant built using Hugging Face Transformers. It can detect emotions from user input, offer motivational and empathetic responses, track goals, and engage in simple mental health check-ins.

# Features
✅ Emotion detection using a fine-tuned DistilBERT model

✅ Smart responses using zero-shot-classification with BART

✅ Handles inputs like “I need help”, stress, motivation, etc.

✅ Weekly goal tracking

✅ Lightweight and fast to load

✅ Runs on Hugging Face Spaces (Gradio or Streamlit compatible)

# How It Works
The chatbot uses two models:

Emotion Predictor (DistilBERT):

Classifies input into 28 possible emotional states like joy, sadness, anxiety, etc.

Wellness Chatbot (facebook/bart-large-mnli):

Uses zero-shot classification to detect themes (stress, motivation, happiness, etc.) and generate relevant responses.

# Installation
Clone the repo and install dependencies:

bash
Copy
Edit
git clone the repo
cd into the folder
pip install -r requirements.txt

# Project Structure
bash
Copy
Edit
.
├── app.py               # Entry point for the chatbot UI
├── core.py              # Main logic for emotion prediction and chatbot
├── model/               # Optional: Local model files
├── requirements.txt     # Python dependencies
├── README.md            # This file

# Requirements
Here's what the app uses:

txt
Copy
Edit
transformers
datasets
torch
scikit-learn
pandas
numpy
tqdm

# Run Locally
bash
Copy
Edit
python app.py
Make sure your core.py and app.py are in the same directory.

# Customize
You can:

Modify the emotion labels in core.py to match your dataset

Expand the candidate_labels in the chatbot for better zero-shot topics

Add memory or journaling features for richer conversations

# FAQ
Q: Does this require GPU?

No, it works on CPU too, though slower.

Q: Can I fine-tune the model?

Yes. But this version uses pretrained models, so no training is needed.

Q: How do I deploy to Hugging Face Spaces?

Just push this repo to a new Space and it will auto-deploy.

# Inspired by
Hugging Face Transformers

Mental health apps like Wysa and Woebot
