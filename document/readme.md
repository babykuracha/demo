**HematoVision - Advanced Blood Cell Classification using Transfer Learning**

---

### 1. Project Overview

HematoVision is a deep learning-based medical imaging project focused on classifying blood cell images. It utilizes MobileNetV2, a lightweight and efficient transfer learning model, to categorize images of blood cells into three classes: Red Blood Cells (RBC), White Blood Cells (WBC), and Platelets. The solution aims to assist in automating microscopic blood analysis for clinical diagnostics.

---

### 2. Objectives

* Automate the classification of blood cell images into RBC, WBC, and Platelets.
* Apply transfer learning to enhance model accuracy and reduce training time.
* Evaluate the model using key performance metrics.
* Optionally, deploy the model via a simple web interface using Streamlit.

---

### 3. Dataset Information

* **Source**: Kaggle - Blood Cells Image Dataset by unclesamulus
* **Classes**: RBC, WBC, Platelets
* **Folder Structure**:

  ```
  blood_cells_dataset/
  └── Blood cells/
      ├── Train/
      ├── Valid/
      └── Test/
  ```

---

### 4. Methodology

#### 4.1 Data Preprocessing

* Resize images to 224x224
* Normalize pixel values
* Use ImageDataGenerator for efficient batch processing

#### 4.2 Model Architecture

* **Base**: MobileNetV2 (pretrained on ImageNet, top removed)
* **Custom Head**:

  * GlobalAveragePooling2D
  * Dense(128, ReLU activation)
  * Dense(3, Softmax activation)
* **Frozen layers**: All base layers frozen
* **Loss Function**: Categorical Crossentropy
* **Optimizer**: Adam
* **Callback**: EarlyStopping (patience=5)

#### 4.3 Training

* Epochs: Up to 15
* Batch Size: 32
* Validation and test evaluations included

---

### 5. Evaluation Metrics

* Accuracy
* Loss Curves
* Confusion Matrix
* Classification Report (Precision, Recall, F1-Score)

---

### 6. Model Deployment

* Model saved as `hematovision_model.h5`
* Optionally deploy using Streamlit with a simple image uploader interface

---

### 7. Requirements

```
tensorflow
tensorflow-hub
numpy
matplotlib
seaborn
scikit-learn
opencv-python
streamlit
```

---

### 8. Conclusion

HematoVision successfully applies transfer learning to the task of classifying blood cells, demonstrating strong performance with minimal training. It provides a promising solution for automating blood analysis workflows in medical diagnostics.

