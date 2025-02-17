# CaptchaSolver-AudioImage-ML
Report on Captcha Processing Project

1. Introduction
This report provides an overview of the Captcha processing project, including the technologies used, the processing workflow, and installation instructions. The project involves handling both image-based and audio-based Captchas stored on Google Drive, preprocessing them, and extracting textual information from images using Optical Character Recognition (OCR) and an LSTM-based model.

2. Technologies Used

Google Colab: Used as the primary development environment.

Python: The programming language for implementation.

OpenCV (cv2): For image preprocessing techniques.

Pytesseract (Tesseract-OCR): For extracting text from Captcha images.

PIL (Pillow): For image handling.

Matplotlib: For visualizing images.

IPython.display: For handling and playing audio files.

TensorFlow/Keras: For building and training the LSTM model.

3. Data Handling

Captcha dataset is stored in Google Drive and mounted in Colab.

Two types of Captchas: Audio-based (WAV files) and Image-based (PNG files).

File paths are structured as:

audio_path = "/content/drive/MyDrive/captchas/audio"

image_path = "/content/drive/MyDrive/captchas/images"

4. Processing Workflow
Step 1: Data Loading

Mount Google Drive and access the dataset.

List available audio and image Captcha files.

Display a sample image and play a sample audio file.

Step 2: Image Preprocessing

Convert the image to grayscale using OpenCV.

Apply Gaussian blur to reduce noise.

Apply binary thresholding for text enhancement.

Perform dilation to improve text clarity.

Step 3: Text Extraction and Recognition

Use Pytesseract OCR to extract text from preprocessed images.

Implement an LSTM-based model to improve Captcha recognition.

Train the LSTM model using labeled Captcha images.

Predict the Captcha text using the trained LSTM model.

5. Installation Instructions
To run the project, follow these steps:

Set up the environment in Google Colab

from google.colab import drive
drive.mount('/content/drive')

Install required dependencies

!pip install pytesseract tensorflow keras
!sudo apt install tesseract-ocr

Import necessary libraries

import cv2
import pytesseract
import numpy as np
from PIL import Image
import matplotlib.pyplot as plt
import tensorflow as tf
from tensorflow import keras

Run the provided notebook to process images and extract text using LSTM

6. Conclusion
This project successfully processes Captcha images using OCR and LSTM-based recognition techniques. Future improvements may include handling distorted Captchas, improving recognition accuracy, and incorporating audio Captcha processing techniques.

