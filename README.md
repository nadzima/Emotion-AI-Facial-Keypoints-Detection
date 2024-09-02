# Facial Keypoints Detection with Machine Learning

This repository contains code for detecting facial keypoints using a dataset of facial images. Each image is 96x96 pixels in grayscale, and the goal is to predict 15 keypoints corresponding to different elements of the face.

## Dataset

**KeyFacialPoints.csv**  
This dataset contains 7049 images of faces, each with corresponding (x, y) coordinates for 15 keypoints on the face:
- **left_eye_center**
- **right_eye_center**
- **left_eye_inner_corner**
- **left_eye_outer_corner**
- **right_eye_inner_corner**
- **right_eye_outer_corner**
- **left_eyebrow_inner_end**
- **left_eyebrow_outer_end**
- **right_eyebrow_inner_end**
- **right_eyebrow_outer_end**
- **nose_tip**
- **mouth_left_corner**
- **mouth_right_corner**
- **mouth_center_top_lip**
- **mouth_center_bottom_lip**

### Missing Data
Some images have missing keypoint values, represented by empty entries between commas in the CSV file.

### Image Data
The image data is provided as a list of integers representing pixel values (0-255), ordered row by row. Each image is 96x96 pixels.

### Data Source
The dataset used for this project can be downloaded from Kaggle's **Facial Keypoints Detection** competition page:  
[https://www.kaggle.com/c/facial-keypoints-detection/data](https://www.kaggle.com/c/facial-keypoints-detection/data)

## Project Structure

- **KeyFacialPointsDetection.ipynb**: Jupyter notebook containing the code for loading the data, preprocessing images, training a machine learning model, and making predictions.
- **KeyFacialPoints.csv**: The dataset used for training and testing the model.
- **README.md**: This file, providing an overview of the project.

## Model Architecture

The machine learning model used in this project is designed to predict the (x, y) coordinates of the 15 keypoints based on the input facial image. The key stages of the model are:

1. **Data Preprocessing**:  
   The images are normalized, and missing keypoints are handled appropriately.

2. **Data Augmentation**:  
   To improve the model's performance and make it more robust, the training data is augmented with techniques such as rotation, scaling, and horizontal flipping. This helps the model generalize better to unseen data by increasing the diversity of the training dataset.

3. **Model Training**:  
   A neural network is trained to predict the keypoints for each image. The network uses layers of convolutions followed by dense layers to output the final predictions for the keypoints.

4. **Evaluation**:  
   The model's performance is evaluated using a mean squared error (MSE) loss function. The predicted keypoints are compared to the ground truth to measure accuracy.

## Source and Documentation

This project is part of a Guided Project on Coursera. The documentation and implementation follow the instructions provided during the course.
