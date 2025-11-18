# face-recognition
Face recognition project using OpenCV, Haarcascade, and a CNN. Includes data collection, preprocessing, training, and real-time recognition through an IP Webcam.
Complete Face Recognition Pipeline:

📸 collect_data.py – Capture 100 face samples per user from IP Webcam

🧹 consolidated_data.py – Resize, grayscale, normalize, and label image data

🧠 Training Notebook – Build & train face recognition CNN model

🔍 recognize.py – Real-time recognition using trained model

🧰 haarcascade_frontalface_default.xml – Face detection

📦 final_model.h5 – Trained neural network

A fully working ML project that demonstrates data collection → preprocessing → model training → deployment.

Here is a **complete, professional, production-ready README.md** for your Face Recognition project.
You can **copy–paste it directly into GitHub**.

---

# 📘 **Face Recognition System using OpenCV & Deep Learning**

This project implements a complete **Face Recognition Pipeline** using **OpenCV**, **Haarcascade**, and a **CNN-based model** built with **Keras/TensorFlow**.
It includes:

* ✔ Face data collection
* ✔ Dataset consolidation & preprocessing
* ✔ Model training (CNN)
* ✔ Real-time face detection & recognition using IP Webcam
* ✔ Organized folder structure with images & processed data

---

## 📂 **Project Structure**

```
Face-Recognition/
│
├── images/                        # Raw face samples (100 per person)
│     ├── John_0.jpg
│     ├── John_1.jpg
│     └── ...
│
├── data/                          # Processed dataset for training
│     ├── images.p
│     └── labels.p
│
├── haarcascade_frontalface_default.xml   # Haarcascade for face detection
│
├── collect_data.py                # Capture face images from IP Webcam
├── consolidated_data.py           # Preprocess + save data as pickle files
├── recognize.py                   # Real-time recognition script
├── final_model.h5                 # Trained CNN model
│
└── README.md                      # Documentation
```

---

## 🚀 **Features**

* 📸 Capture 100 face images per person using an IP Webcam
* 🧹 Preprocess data: crop → resize → grayscale → normalize
* 🗂 Automatic labeling based on filenames
* 🧠 Train a CNN model for face classification
* 🎥 Real-time face detection & recognition
* 🔍 Uses Haarcascade for face detection
* 🌐 IP Webcam support (Android app recommended)

---

## 🛠️ **Technologies Used**

* **Python**
* **OpenCV**
* **NumPy**
* **Keras / TensorFlow**
* **Matplotlib**
* **Pickle**
* **Haarcascade**

---

## 📥 **1. Collecting Data (Face Samples)**

Use `collect_data.py` to capture face images from your IP Webcam.

### **Requirements**

Install IP Webcam from Play Store → Start server → copy its URL.

Edit the URL inside the script:

```python
url = "http://YOUR_IP:8080/shot.jpg"
```

### **Run the script**

```
python collect_data.py
```

You’ll be prompted to enter the person’s name (e.g., "John").
It saves 100 face images in:

```
images/<name>_0.jpg ... <name>_99.jpg
```

---

## 🧹 **2. Preprocessing & Dataset Creation**

Run `consolidated_data.py` to:

* Resize images → 100×100
* Grayscale conversion
* Extract labels
* Save into **images.p** and **labels.p**

### Run:

```
python consolidated_data.py
```

The following files will be created under **data/**:

```
data/images.p
data/labels.p
```

---

## 🧠 **3. Model Training**

Training is done using a CNN model (usually built in a Jupyter notebook).
The final trained model is stored as:

```
final_model.h5
```

If you want, I can generate the full training notebook for you.

---

## 🎯 **4. Real-Time Face Recognition**

Use the script `recognize.py` to run real-time recognition via IP Webcam.

### Run:

```
python recognize.py
```

It will:

* Detect faces using Haarcascade
* Preprocess the face
* Predict the person’s identity
* Display the video feed with labels

---

## 🗂️ **Folder Descriptions**

### **images/**

Contains raw face samples captured using `collect_data.py`.
Each file is named as:

```
<person_name>_<index>.jpg
```

Used for preprocessing and training.

---

### **data/**

Contains two pickle files created by `consolidated_data.py`:

| File         | Description                                                   |
| ------------ | ------------------------------------------------------------- |
| **images.p** | Preprocessed grayscale 100x100 images stored as a NumPy array |
| **labels.p** | Labels extracted from filenames                               |

These files are used during model training.

---

## ⚙️ **Installation**

Install dependencies:

```
pip install opencv-python numpy keras tensorflow matplotlib
```

---

## ▶️ **How to Run the Entire Pipeline**

### **Step 1: Capture images**

```
python collect_data.py
```

### **Step 2: Preprocess and save dataset**

```
python consolidated_data.py
```

### **Step 3: Train the model**

Use your training notebook (or ask me to generate one).

### **Step 4: Run real-time recognition**

```
python recognize.py
```

---

## 📝 **Notes**

* Ensure your Haarcascade XML file path is correct in the scripts.
* IP Webcam and PC must be on the same Wi-Fi network.
* Collect at least 100 images per person for better accuracy.

---

## 📄 **License**

This project is licensed under the **MIT License**.

---

## 🙌 **Contributions**

Pull requests are welcome!
Feel free to open issues for suggestions or errors.

---
