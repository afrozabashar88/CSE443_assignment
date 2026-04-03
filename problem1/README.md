
##  Objective

The objective of this project is to build a Convolutional Neural Network (CNN) model to classify chest X-ray images as **PNEUMONIA** or **NORMAL**.

## 📊 Dataset

* Dataset: Chest X-ray Images
* Classes:

  * NORMAL
  * PNEUMONIA
* Total Images:

  * Training: 5216
  * Validation: 16
  * Test: 624


##  Methodology

###  Data Preprocessing

* Images resized to **150 × 150**
* Normalization using rescaling (1/255)
* Data augmentation applied:

  * Shear transformation
  * Zoom
  * Horizontal flip

###  Model Architecture

A Convolutional Neural Network (CNN) was built using:

* 3 Convolutional layers (32, 64, 128 filters)
* MaxPooling layers
* Flatten layer
* Fully connected Dense layer (128 neurons)
* Dropout (0.5) to reduce overfitting
* Output layer with sigmoid activation

###  Compilation

* Optimizer: Adam
* Loss Function: Binary Crossentropy
* Metrics: Accuracy

---

##  Training

* Epochs: 10
* Batch Size: 32

---

##  Results

###  Test Accuracy

* **91.18%**

###  Confusion Matrix


[[190  44]
 [ 11 379]]


###  Classification Report

* Accuracy: 91%
* Precision (NORMAL): 0.95
* Precision (PNEUMONIA): 0.90
* Recall (NORMAL): 0.81
* Recall (PNEUMONIA): 0.97



##  Observations

* Model performs better in detecting **PNEUMONIA** than NORMAL cases
* Slight imbalance in validation dataset affects validation accuracy
* Overfitting is controlled using dropout and augmentation




