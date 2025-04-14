
---
# Myopia Detection Using Deep Learning

This project leverages state-of-the-art deep learning models to detect **myopia** (nearsightedness) from **retinal fundus images**. The models used in this project include **CoAtNet**, **ResNet-50**, and **YOLOv5**. This approach aims to improve the accuracy and efficiency of early myopia detection, which is critical for preventing vision impairment.

## Table of Contents
- [Overview](#overview)
- [Models Used](#models-used)
- [Project Setup](#project-setup)
- [Dataset](#dataset)
- [Installation](#installation)
- [Results](#results)
- [Evaluation](#evaluation)
- [Contributions](#contributions)
- [License](#license)

## Overview
The project implements deep learning models for myopia detection using **CoAtNet**, **ResNet-50**, and **YOLOv5**. The models were trained on retinal fundus images to classify whether a person has myopia or not. The key objective is to demonstrate high accuracy and robustness using these cutting-edge models.

## Models Used
### CoAtNet
- **CoAtNet** is a hybrid model combining convolutional layers and transformers, which helps capture both local and global features in the retinal images.
- Achieved **98.6% accuracy** in detecting myopia.

### ResNet-50
- **ResNet-50** is a residual network used as a baseline for comparison. It helps mitigate the vanishing gradient problem by using skip connections.
- Achieved **85% accuracy** on the dataset.

### YOLOv5
- **YOLOv5** is used for object detection to localize regions of interest in the fundus images. YOLO helps highlight the pathological markers contributing to myopia.
- Achieved **95% accuracy** for detecting myopia-related features.

## Project Setup

### Dataset
- The dataset consists of retinal fundus images annotated for **myopia** and **non-myopia** classes. It was sourced from publicly available ophthalmic image datasets.
- The images are preprocessed using **OpenCV**, including normalization, resizing, and data augmentation techniques like random rotations and flips.

### Installation

#### Requirements
The project requires the following Python libraries:
- **TensorFlow** or **PyTorch** (depending on the model implementation)
- **OpenCV** for image processing
- **NumPy** for numerical operations
- **Matplotlib** and **Seaborn** for visualizations
- **scikit-learn** for performance evaluation

You can install the necessary libraries using `pip`:

```bash
pip install tensorflow opencv-python numpy matplotlib seaborn scikit-learn
```

### Clone the Repository
To clone the project repository:

```bash
git clone https://github.com/sanuthreddy/DetectionofMyopia.git
cd Myopia-Detection
```

### Training the Models
To train the models, run the training scripts for each model:

1. **CoAtNet**: 
   - `python train_coatnet.py`
2. **ResNet-50**: 
   - `python train_resnet.py`
3. **YOLOv5**:
   - `python train_yolov5.py`

### Evaluation
You can evaluate the trained models using the evaluation script:

```bash
python evaluate.py
```

This will output the evaluation metrics such as **accuracy**, **precision**, **recall**, and **F1-score**.

## Results
### CoAtNet:
- **Accuracy**: 98.6%
- **Precision**: 0.98
- **Recall**: 0.99
- **F1-score**: 0.985

### ResNet-50:
- **Accuracy**: 85%
- **Precision**: 0.83
- **Recall**: 0.85
- **F1-score**: 0.84

### YOLOv5:
- **Accuracy**: 95%
- **Precision**: 0.94
- **Recall**: 0.96
- **F1-score**: 0.95

## Evaluation
The models were evaluated using various metrics:
- **Accuracy**: Overall correctness of the model.
- **Precision**: Measures the proportion of correctly predicted positives.
- **Recall**: Measures the proportion of actual positives correctly identified by the model.
- **F1-score**: Harmonic mean of precision and recall, used to balance both metrics.

## Contributions
Feel free to fork the project and contribute improvements, such as:
- **Adding more datasets** for training
- **Implementing additional models** (e.g., EfficientNet, VGG)
- **Enhancing data augmentation** techniques

## License
This project is licensed under the MIT License.

---

