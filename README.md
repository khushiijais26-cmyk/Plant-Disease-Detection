# Plant Disease Detection Using CNN

## Overview

This project is an AI-based Plant Disease Detection system that uses a Convolutional Neural Network (CNN) to identify plant diseases from leaf images.

The model is trained using the PlantVillage dataset and can classify leaf images into 15 different plant disease and healthy-leaf categories.

## Features

- Image-based plant disease detection
- CNN-based deep learning model
- 15 disease/healthy-leaf classes
- Image preprocessing and normalization
- Model evaluation using accuracy, precision, recall and F1-score
- Confusion matrix visualization
- Prediction on individual leaf images

## Dataset

The project uses the PlantVillage dataset.

The dataset contains 20,638 images belonging to 15 classes.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Pillow
- Jupyter Notebook

## Model Architecture

The CNN consists of:

- 3 Convolutional layers
- Max Pooling layers
- Fully Connected Dense layer
- Dropout layer
- Softmax output layer

Input image size:

128 × 128 × 3

Number of output classes:

15

## Model Performance

The model was trained for 10 epochs.

Final validation accuracy:

**91.50%**

Best validation accuracy observed during training:

**92.71%**

Classification report:

- Macro F1-score: 0.90
- Weighted F1-score: 0.92

## Sample Prediction

The trained model was tested on an individual leaf image.

Example result:

**Predicted Disease:** Tomato Late Blight

**Confidence:** 98.71%

## Project Structure

```text
Plant disease detection/
│
├── data/
│   └── PlantVillage/
│
├── model/
│   └── plant_disease_model.keras
│
├── notebook/
│   └── plant_disease_detection.ipynb
│
├── reports/
│
├── test_images/
│   └── test.jpg
│
├── requirements.txt
└── README.md