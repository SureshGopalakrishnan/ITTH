# Brain Tumor MRI Classification using a Convolutional Neural Network (CNN)

This project implements a deep learning solution for multi-class classification of brain tumors from MRI scans. It utilizes a **Convolutional Neural Network (CNN)** built with TensorFlow/Keras to distinguish between three types of tumors and healthy (no tumor) brains.

## Assignment Goal

The primary objective is to develop a robust, high-accuracy model that can assist medical professionals by automatically and accurately classifying the following conditions from MRI images:

1.  **Glioma**
2.  **Meningioma**
3.  **Pituitary**
4.  **No Tumor** (Healthy Brain)

## Dataset Overview

The model is trained and evaluated on a comprehensive dataset containing over 7,000 brain MRI images. The data is structured into `Training` and `Testing` folders, with subfolders corresponding to the four target classes:

| Class Name | Description |
| :--- | :--- |
| `glioma` | Tumors originating from glial cells. |
| `meningioma` | Tumors arising from the meninges. |
| `notumor` | Healthy brains with no tumor present. |
| `pituitary` | Tumors located in the pituitary gland. |

## Features & Methodology

The Python script (`BrainTumourMRI_CNN.py`) performs the entire machine learning pipeline, including data preparation and model training:

### 1. Data Loading and Preprocessing
* **Image Loading:** All images are recursively loaded from the directory structure.
* **Resizing:** Images are resized to a consistent 150 × 150 pixel format.
* **Normalization:** Pixel values are scaled from 0-255 to 0.0-1.0 to aid model convergence.
* **Label Encoding:** Class labels are converted into numerical and then **One-Hot Encoded** vectors, which is required for the `categorical_crossentropy` loss function.

### 2. CNN Architecture
The CNN model uses a sequential design focused on robust feature extraction:
* A series of **Convolutional Layers** (`Conv2D`) with `relu` activation and increasing filter sizes ($32 \rightarrow 64 \rightarrow 128$).
* **MaxPooling Layers** (`MaxPool2D`) are used after each convolution block to reduce dimensionality and retain important features.
* A **Flatten Layer** converts the 2D feature maps into a 1D vector.
* A final **Dense Layer** with **`softmax`** activation outputs the classification probabilities for the 4 classes.

### 3. Training and Evaluation
* The model is compiled using the **Adam optimizer** and **categorical cross-entropy loss**.
* Model performance is evaluated on the dedicated test set, reporting **Accuracy**, **Loss**, and a detailed **Confusion Matrix** to analyze class-specific performance.

The program handles data loading, model definition, training, and final evaluation, outputting the training history and classification report.

## Next Steps and Improvements

To further enhance the model's performance, stability, and utility, the following areas should be explored:

### 1. Advanced Data Handling
* **Data Augmentation:** Implement real-time image augmentation (rotation, shearing, zooming, shifting) during training to increase the effective size and diversity of the training set, which helps prevent overfitting.
* **Class Balancing:** Investigate techniques like SMOTE or weighted loss functions if the training set exhibits significant class imbalance.

### 2. Model Architecture Enhancements
* **Transfer Learning:** Utilize pre-trained models like **VGG16**, **ResNet**, or **Inception** (Transfer Learning) to leverage features learned from millions of general-purpose images. This often leads to faster convergence and higher accuracy, especially on smaller datasets.
* **Hyperparameter Tuning:** Systematically test different learning rates, batch sizes, and optimizer configurations (e.g., using techniques like Grid Search or Randomized Search).

### 3. Deepening Evaluation and Interpretation
* **Gradient-weighted Class Activation Mapping (Grad-CAM):** Implement Grad-CAM to visualize which parts of the MRI image the CNN is focusing on when making a prediction. This is essential for building trust and verifying the model's clinical relevance.
* **K-Fold Cross-Validation:** For a more robust estimate of the model's generalization ability, implement K-Fold Cross-Validation instead of a single train/test split.
