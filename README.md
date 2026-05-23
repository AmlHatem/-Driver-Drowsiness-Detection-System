# 🚗 Driver Drowsiness Detection System

An Image Processing and Machine Learning project designed to detect whether a driver is drowsy or alert in real time.

The system analyzes driver facial and eye features using computer vision techniques to improve road safety and reduce accidents caused by driver fatigue.

---

# 🚀 Project Overview

Driver drowsiness is one of the major causes of road accidents worldwide.

This project uses:
- Image Processing
- Computer Vision
- Machine Learning

to detect signs of driver fatigue from images.

The model classifies drivers into:
- **Drowsy**
- **Non Drowsy**

---

# 🧠 Project Idea

The system works by:
1. Detecting the driver's face.
2. Detecting the eyes region.
3. Processing the eye image using image processing techniques.
4. Extracting important visual features.
5. Predicting whether the driver is sleepy or awake.

---

# 📂 Dataset

The dataset was collected from Kaggle and divided into two classes:

- Drowsy
- Non Drowsy

Additional external images were also used to test the model performance on unseen data.

---

# 🛠️ Technologies Used

- Python
- OpenCV
- NumPy
- Scikit-learn
- Joblib

---

# 🧠 Machine Learning Model

## 🔹 Support Vector Machine (SVM)

The project uses a Linear Support Vector Machine classifier:

```python
LinearSVC(max_iter=10000)
```

### ✅ Why SVM?
- Works efficiently with image classification problems
- Performs well on binary classification tasks
- Fast and lightweight model
- Suitable for processed edge-based image features

### 📌 Used For
- Classifying driver state
- Detecting drowsiness
- Predicting alert vs sleepy conditions

---

# 🖼️ Image Processing Techniques Used

## 🔹 Face Detection
The system uses Haar Cascade classifiers to detect faces from images.

```python
haarcascade_frontalface_default.xml
```

---

## 🔹 Eye Detection
Eye regions are extracted for detailed analysis.

```python
haarcascade_eye.xml
```

---

## 🔹 CLAHE (Contrast Enhancement)

CLAHE is used to improve image lighting and contrast.

### Benefits
- Enhances low-light images
- Improves feature visibility
- Makes detection more accurate

---

## 🔹 Gaussian Blur

Used to reduce image noise before feature extraction.

---

## 🔹 Canny Edge Detection

Used to extract important eye features and edges.

```python
cv2.Canny()
```

### Why Edge Detection?
- Highlights eye structure
- Helps distinguish open and closed eyes
- Improves model accuracy

---

## 🔹 Data Augmentation

Horizontal image flipping was applied to increase dataset size and improve model generalization.

```python
cv2.flip()
```

---

# ⚙️ System Workflow

## 🔹 Step 1: Load Dataset
Images are loaded from:
- Drowsy folder
- Non Drowsy folder

---

## 🔹 Step 2: Preprocessing
The system performs:
- Grayscale conversion
- CLAHE enhancement
- Face detection
- Eye extraction
- Gaussian blur
- Edge detection

---

## 🔹 Step 3: Training
The processed images are flattened and used to train the SVM model.

---

## 🔹 Step 4: Evaluation
The model is evaluated using test data to calculate accuracy.

---

## 🔹 Step 5: Testing
New external images are tested to predict:
- Drowsy
- Non Drowsy

The result is displayed directly on the image using OpenCV.

---

# 📊 Features

✅ Real-time prediction capability  
✅ Face and eye detection  
✅ Image preprocessing pipeline  
✅ Lightweight and fast model  
✅ Edge-based feature extraction  
✅ External image testing support  

---

# ▶️ How to Run

```bash
# Clone repository
git clone https://github.com/your-username/your-repository-name.git

# Open project folder
cd your-repository-name

# Install dependencies
pip install -r requirements.txt

# Run project
python main.py
```

---

# 📈 Future Improvements

- Real-time webcam integration
- Alarm system for sleepy drivers
- Deep Learning implementation (CNN)
- Mobile application support
- Night vision optimization
- Real-time video stream detection

---

# 📌 Project Goals

- Improve road safety using AI
- Detect driver fatigue automatically
- Apply Image Processing techniques in real-world problems
- Build an intelligent driver monitoring system

---

# 👩‍💻 Author

Developed as an Image Processing and Machine Learning project for educational and research purposes.
