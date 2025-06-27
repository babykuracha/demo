**HematoVision - Advanced Blood Cell Classification using Transfer Learning (Design Thinking Approach)**

---

### 1. Empathize: Understanding the Problem

Manual classification of blood cells under a microscope is time-consuming, prone to human error, and requires expert knowledge. Misclassification can lead to incorrect medical diagnoses. To address these challenges, we sought to understand the needs of lab technicians and pathologists, emphasizing speed, accuracy, and accessibility.

---

### 2. Define: Problem Statement

Medical laboratories need an efficient and accurate system to automate the classification of Red Blood Cells (RBCs), White Blood Cells (WBCs), and Platelets from microscopic images to support clinical diagnosis.

---

### 3. Ideate: Exploring Solutions

* Use deep learning for image classification.
* Apply transfer learning to overcome limited data.
* Implement a lightweight model for ease of deployment.
* Create a simple and user-friendly web interface for real-time use.

---

### 4. Prototype: Model Development

* **Dataset**: Kaggle - Blood Cells Image Dataset
* **Folder Structure**:

  ```
  blood_cells_dataset/
  └── Blood cells/
      ├── Train/
      ├── Valid/
      └── Test/
  ```
* **Preprocessing**:

  * Resized to 224x224
  * Normalized pixel values
* **Model**: MobileNetV2 with custom dense layers
* **Training**:

  * 15 Epochs with EarlyStopping
  * Optimizer: Adam
  * Loss: Categorical Crossentropy

---

### 5. Test: Evaluation and Validation

* Evaluated on validation and test sets
* Metrics:

  * Accuracy
  * Confusion Matrix
  * Classification Report (Precision, Recall, F1-Score)
* Visualization:

  * Loss and accuracy curves
  * Confusion matrix heatmap

---

### 6. Implement: Deployment and Impact

* Saved model as `hematovision_model.h5`
* Streamlit app for real-time classification with image upload interface
* Reduced workload for lab staff
* Increased consistency in diagnostic support

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

By applying the design thinking methodology, HematoVision was developed with a human-centered approach. It successfully automates blood cell classification while being fast, accurate, and easy to use—ultimately aiming to support medical professionals in their diagnostic tasks.
