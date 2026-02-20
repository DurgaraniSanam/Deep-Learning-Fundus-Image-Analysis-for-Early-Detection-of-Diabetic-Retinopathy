# 🩺 Deep-Learning-Fundus-Image-Analysis-for-Early-Detection-of-Diabetic-Retinopathy


## 📌 Overview
This project focuses on detecting **Diabetic Retinopathy (DR)** from retinal fundus images using a deep learning model based on **Xception transfer learning architecture**.

Diabetic Retinopathy is a serious complication of diabetes that can lead to vision loss if not detected early. This system helps in identifying the disease at different stages by analyzing retinal images automatically using AI.

The project consists of:
- Deep learning model training
- Model evaluation
- Flask web application
- Image upload and real-time prediction
- User login and registration system

---

## 🧠 Model Details
- **Base Architecture:** Xception (Transfer Learning)
- **Input Image Size:** 299 × 299 × 3
- **Number of Classes:** 5
- **Optimizer:** Adam
- **Loss Function:** Categorical Crossentropy
- **Output Activation:** Softmax
- **Framework:** TensorFlow / Keras

The pre-trained Xception network is used for feature extraction and additional dense layers are added for classification.

---

## 🏷 Classification Labels

| Class | Condition |
|------|-----------|
| 0 | No Diabetic Retinopathy |
| 1 | Mild |
| 2 | Moderate |
| 3 | Severe |
| 4 | Proliferative |

---

## 📂 Dataset Structure

```
dataset/
 ├── training/
 │    ├── 0
 │    ├── 1
 │    ├── 2
 │    ├── 3
 │    └── 4
 └── testing/
      ├── 0
      ├── 1
      ├── 2
      ├── 3
      └── 4
```

### 🔗 Resources
**Trained Model (.h5):**  
https://drive.google.com/file/d/1jaWRc_l10clG6lhPosO6ee5Vh5mKrjJD/view  

**Dataset:**  
https://www.kaggle.com/datasets/arbethi/diabetic-retinopathy-level-detection  

---

## ⚙️ Workflow

### 1. Data Preprocessing
- Images resized to 299×299
- Xception preprocessing applied
- Data augmentation used during training

### 2. Model Training
- Loaded Xception without top layer
- Added custom dense layers
- Trained on dataset
- Saved trained model in `.h5` format

### 3. Model Evaluation
- Accuracy and loss graphs generated
- Confusion matrix plotted
- Class distribution visualized

These metrics help understand model performance and detect overfitting.

---

## 🌐 Flask Web Application

The trained model is integrated into a Flask-based web application.

### Pages Included
**Home Page**
- Landing interface
- Navigation options

**Login Page**
- User authentication

**Register Page**
- New user registration

**Prediction Page**
- Upload retinal image
- Displays predicted class and confidence score

---

## 🔍 Prediction Process
1. User uploads a retinal image.
2. Image is converted from BGR to RGB.
3. Image resized to 299×299.
4. Xception preprocessing applied.
5. Model predicts class probabilities.
6. Highest probability class selected.
7. Result displayed on screen.

---

## 🛠 Technologies Used
- Python
- TensorFlow / Keras
- Flask
- OpenCV
- NumPy
- Matplotlib
- HTML
- CSS
- Bootstrap

---

## 🚀 How to Run the Project

### Install dependencies
```bash
pip install tensorflow flask numpy opencv-python matplotlib
```

### Place model file
Put the trained model file in the project folder:
```
Updated-xception-diabetic-retinopathy.h5
```

### Run Flask app
```bash
python app.py
```

### Open browser
```
http://127.0.0.1:5000/
```

---

## 📊 Example Output
Uploaded Image → Predicted Class: Moderate DR  
Confidence score displayed with result.

---

## 📄 Conclusion
This project demonstrates how transfer learning with the Xception model can be used for multi-class classification of diabetic retinopathy. The integration with a Flask web application allows users to upload retinal images and obtain predictions instantly. This approach can support early detection and assist healthcare professionals in screening patients efficiently.
