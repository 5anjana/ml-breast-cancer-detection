# Histopathologic Cancer Detection with CNN
This project aims to identify metastatic cancer in histopathologic scans of lymph node sections using a Convolutional Neural Network (CNN). The dataset is sourced from the [Kaggle Histopathologic Cancer Detection challenge](https://www.kaggle.com/competitions/histopathologic-cancer-detection/overview). 

---

## Dataset Description

The dataset consists of small pathology image patches:

- train/ — Folder of labeled training images
- test/ — Folder of unlabeled test images
- train_labels.csv — Contains image IDs and binary labels (1 = tumor, 0 = no tumor)
- sample_submission.csv — Template for test predictions

Each image is a 96×96 pixel RGB patch. A label of 1 means the center 32×32px region contains tumor tissue. The surrounding area is included to support convolutional models without zero-padding.

---

## Model Architecture

A custom CNN with 5 convolutional layers is used to classify images. The model pipeline includes:

- Input normalization
- Convolutional + ReLU + MaxPooling layers
- Fully connected layers
- Sigmoid output for binary classification

The model is trained using binary cross-entropy loss.
