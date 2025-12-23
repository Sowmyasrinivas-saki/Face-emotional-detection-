# Face Emotion Detection Project

📌 Project Overview
This project detects human facial emotions from images using computer vision and deep learning techniques.
You place images into the project folder, and the system automatically:
Detects faces in the image
Analyzes facial features
Predicts the dominant emotion for each detected face
If you think this is “just image classification”, you’re wrong — it’s face detection + emotion classification, two different problems.

🎯 Emotions Detected
The model predicts one of the following emotions:
Angry
Disgust
Fear
Happy
Sad
Surprise
Neutral
These are standard FER (Facial Emotion Recognition) classes. If your model claims more, it’s probably lying.

🧠 How It Works (Concept — Understand This)
Image Input
Images are read from a specified folder
Supported formats: .jpg, .jpeg, .png

Face Detection
Uses Haar Cascade / DNN / MTCNN (depending on implementation)
Locates face regions inside the image
If no face is found → no emotion is predicted

Preprocessing
Face is resized (usually 48×48 or 224×224)
Converted to grayscale or normalized RGB
Pixel values scaled (0–1)

Emotion Classification
A trained CNN model predicts emotion probabilities
The emotion with highest confidence is selected

Output
Emotion label displayed on the face
Bounding box drawn around detected face
