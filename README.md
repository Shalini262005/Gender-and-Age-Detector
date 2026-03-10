# Gender and Age Detection using CNN

This project implements a Gender and Age Detection system that predicts the gender and approximate age of a person from an image or video frame. The model is built using a Convolutional Neural Network (CNN) and uses OpenCV for image processing and feature extraction.

The system analyzes facial images and predicts demographic attributes by identifying patterns and features learned during training.

---

## Project Overview

The objective of this project is to build a deep learning model capable of identifying the age and gender of a person from facial images. The system uses computer vision techniques combined with deep learning to extract meaningful features from images and classify them.

The workflow of the system includes:

1. Detecting faces from an image or video frame.
2. Preprocessing the detected face.
3. Passing the processed image to a trained CNN model.
4. Predicting the gender (Male / Female) and approximate age of the person.

This project demonstrates how deep learning models can be integrated with image processing systems for automated visual analysis.

---

## Dataset

The model was trained using the UTKFace dataset, which is widely used for age and gender prediction tasks.

Dataset Link:  
https://www.kaggle.com/datasets/jangedoo/utkface-new

### Dataset Description

The UTKFace dataset contains thousands of face images labeled with age, gender, and ethnicity. Each image file name includes the label information in the following format:

age_gender_race_date.jpg

Example:
25_0_2_20170116174525125.jpg

Where:
- 25 → Age
- 0 → Gender (0 = Male, 1 = Female)
- 2 → Race
- Date → Timestamp

For this project, the age and gender labels were extracted from the file names and used as the target variables for training the model.

---

## Technologies Used

The following technologies and libraries were used to build this project:

- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Pandas
- Matplotlib

---

## Model Architecture

The model uses a Convolutional Neural Network (CNN) to automatically learn facial features from images.

CNNs are particularly effective for computer vision tasks because they can detect spatial patterns such as edges, shapes, and textures in images.

The model architecture includes:

- Convolutional layers for feature extraction
- Activation layers (ReLU)
- Pooling layers for dimensionality reduction
- Fully connected layers for classification
- Output layers for predicting age and gender

The model learns important facial features during training and uses them to make predictions on new images.

---

## Image Processing using OpenCV

OpenCV is used for performing image processing tasks such as:

- Reading images and video frames
- Detecting faces
- Cropping facial regions
- Resizing images to match the model input size
- Converting images into a format suitable for the CNN model

This allows the system to work with both static images and frames extracted from videos.

---

## Project Workflow

The complete workflow of the system is as follows:

1. Load an image or capture frames from a video.
2. Detect faces in the image using OpenCV.
3. Extract the detected face region.
4. Preprocess the face image (resize and normalize).
5. Pass the processed image to the trained CNN model.
6. Predict the age and gender of the detected person.
7. Display the predicted results on the image or video frame.
