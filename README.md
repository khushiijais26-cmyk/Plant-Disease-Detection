# AI System for Agricultural Tasks

## Overview

This project is an AI-based system developed to assist with agricultural tasks using Machine Learning and Deep Learning techniques.

The project consists of two major components:

- **Part A – Crop Recommendation**
- **Part B – Plant Disease Detection**

The Crop Recommendation component recommends a suitable crop based on agricultural and environmental parameters, while the Plant Disease Detection component identifies plant diseases from leaf images using a Convolutional Neural Network (CNN).

This project was developed as part of the **AISA Lab – Lab Assignment No. 06**.

---

## Project Objectives

The main objectives of this project are:

- To use Artificial Intelligence techniques for agricultural applications.
- To recommend suitable crops based on input soil and environmental conditions.
- To detect plant diseases from leaf images.
- To apply Machine Learning and Deep Learning techniques to real-world agricultural problems.
- To evaluate the performance of the developed models using appropriate evaluation metrics.

---

# Part A – Crop Recommendation

## Description

The Crop Recommendation component uses Machine Learning techniques to recommend a suitable crop based on input agricultural and environmental parameters.

The implementation includes data analysis, preprocessing, model development, evaluation, and crop prediction.

The complete implementation is available in the Jupyter Notebook:

```text
Part-A-Crop-Recommendation/
└── ass6pe(a).ipynb
```

## Workflow

```text
Input Agricultural Parameters
            ↓
      Data Preprocessing
            ↓
      Machine Learning Model
            ↓
       Model Prediction
            ↓
    Recommended Crop
```

---

# Part B – Plant Disease Detection

## Description

The Plant Disease Detection component is a Deep Learning-based system that identifies plant diseases from leaf images.

A Convolutional Neural Network (CNN) is trained using the **PlantVillage dataset** to classify leaf images into different disease and healthy-leaf categories.

## Dataset

The PlantVillage dataset was used for training and validation.

The dataset used in this project contains:

- **Total images:** 20,638
- **Number of classes:** 15
- **Training images:** 16,511
- **Validation images:** 4,127

The complete dataset is not included in this repository because of its size.

## Plant Disease Classes

The model classifies images into the following 15 categories:

1. Pepper – Bacterial Spot
2. Pepper – Healthy
3. Potato – Early Blight
4. Potato – Late Blight
5. Potato – Healthy
6. Tomato – Bacterial Spot
7. Tomato – Early Blight
8. Tomato – Late Blight
9. Tomato – Leaf Mold
10. Tomato – Septoria Leaf Spot
11. Tomato – Spider Mites
12. Tomato – Target Spot
13. Tomato – Yellow Leaf Curl Virus
14. Tomato – Mosaic Virus
15. Tomato – Healthy

---

## Model Architecture

A Convolutional Neural Network (CNN) was developed for plant disease classification.

The model consists of:

- 3 Convolutional layers
- Max Pooling layers
- Fully Connected Dense layer
- Dropout layer
- Softmax output layer

### Input

```text
128 × 128 × 3
```

### Output

```text
15 classes
```

### Model Structure

```text
Input Image
     ↓
Convolutional Layer
     ↓
Max Pooling
     ↓
Convolutional Layer
     ↓
Max Pooling
     ↓
Convolutional Layer
     ↓
Max Pooling
     ↓
Flatten
     ↓
Dense Layer
     ↓
Dropout
     ↓
Softmax Output
     ↓
Predicted Disease Class
```

---

## Data Preprocessing

The input images were resized to:

```text
128 × 128
```

Pixel values were normalized using:

```python
Rescaling(1./255)
```

The dataset was divided into training and validation sets.

---

## Model Training

The CNN model was trained for **10 epochs**.

The model was compiled using:

- **Optimizer:** Adam
- **Loss Function:** Sparse Categorical Crossentropy
- **Output Activation:** Softmax

---

## Model Performance

The model achieved the following results on the validation dataset:

| Metric | Result |
|---|---:|
| Final Validation Accuracy | **91.50%** |
| Best Validation Accuracy | **92.71%** |
| Macro F1-Score | **0.90** |
| Weighted F1-Score | **0.92** |
| Validation Images | **4,127** |

The best validation accuracy of **92.71%** was observed during training at epoch 9.

The final validation accuracy after 10 epochs was **91.50%**.

---

## Evaluation

The model was evaluated using:

- Validation Accuracy
- Precision
- Recall
- F1-Score
- Classification Report
- Confusion Matrix

---

## Sample Prediction

A test leaf image was used for prediction.

```text
Predicted Disease: Tomato Late Blight
Confidence: 98.71%
```

The test image is available in:

```text
test_images/test.jpg
```

---

## Technologies Used

### Programming Language

- Python

### Machine Learning and Deep Learning

- TensorFlow
- Keras
- Scikit-learn

### Data Processing

- NumPy
- Pandas
- Pillow

### Data Visualization

- Matplotlib
- Seaborn

### Development Environment

- Jupyter Notebook
- Python 3.11

---

## Project Structure

```text
Plant-Disease-Detection/
│
├── Part-A-Crop-Recommendation/
│   └── ass6pe(a).ipynb
│
├── model/
│   └── plant_disease_model.keras
│
├── notebook/
│   └── plant_disease_detection.ipynb
│
├── test_images/
│   └── test.jpg
│
├── reports/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/khushiijais26-cmyk/Plant-Disease-Detection.git
```

### 2. Navigate to the Project Directory

```bash
cd Plant-Disease-Detection
```

### 3. Install the Required Packages

```bash
pip install -r requirements.txt
```

### Running Part A

Open:

```text
Part-A-Crop-Recommendation/ass6pe(a).ipynb
```

Run the notebook cells sequentially to perform the Crop Recommendation workflow.

### Running Part B

Open:

```text
notebook/plant_disease_detection.ipynb
```

The notebook contains the complete Plant Disease Detection workflow, including:

1. Dataset loading
2. Data preprocessing
3. Dataset splitting
4. CNN model creation
5. Model compilation
6. Model training
7. Model evaluation
8. Classification report
9. Confusion matrix
10. Individual image prediction

The trained model is stored at:

```text
model/plant_disease_model.keras
```

---

## Trained Model

The trained Plant Disease Detection model is included in the repository:

```text
model/plant_disease_model.keras
```

This allows the trained model to be reused without training the CNN from the beginning.

---

## Dataset Note

The PlantVillage dataset is not included in the GitHub repository because of its large size.

The `data/` directory is excluded using `.gitignore`.

To reproduce the Plant Disease Detection experiment, the required dataset should be placed in the appropriate project data directory before running the notebook.

---

## Key Features

### Crop Recommendation

- Agricultural parameter-based crop recommendation
- Machine Learning-based prediction
- Data preprocessing and analysis
- Notebook-based implementation

### Plant Disease Detection

- Image-based disease classification
- CNN-based Deep Learning model
- 15 plant disease and healthy-leaf classes
- Image preprocessing and normalization
- Model evaluation
- Classification report
- Confusion matrix
- Individual leaf image prediction
- Saved trained model

---

## Results Summary

| Component | Technique | Output |
|---|---|---|
| Part A – Crop Recommendation | Machine Learning | Recommended Crop |
| Part B – Plant Disease Detection | CNN / Deep Learning | Plant Disease Class |

For Part B, the CNN achieved a final validation accuracy of **91.50%**, with a best observed validation accuracy of **92.71%**.

---

## Future Improvements

Possible future improvements include:

- Using data augmentation to improve generalization.
- Experimenting with deeper CNN architectures.
- Using transfer learning with pretrained models.
- Improving performance on visually similar disease classes.
- Developing a web-based interface for easier image-based prediction.
- Integrating both components into a single agricultural assistance application.

---

## Disclaimer

This project is developed for **academic and educational purposes**.

The predictions generated by the models should not be treated as professional agricultural, medical, or plant-health advice. Actual agricultural decisions should be made with appropriate expert guidance.

---

## Author

**Khushi Jaiswal**

Computer Science Engineering – Artificial Intelligence and Data Science
