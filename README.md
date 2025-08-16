# face-recognition
Perfect 🚀 Here’s a clean **README.md** draft you can directly use for your GitHub repo:

---

# 👤 Face Recognition using KNN & OpenCV

This project is a **real-time face recognition system** that uses the **K-Nearest Neighbors (KNN)** algorithm and **OpenCV**. It detects faces from a webcam feed, classifies them based on stored training data, and displays the predicted name in real time.

---

## 📌 Features

* ✅ **Face Detection** using OpenCV’s Haar Cascade.
* ✅ **Face Recognition** with KNN implemented **from scratch** (no scikit-learn).
* ✅ **Real-time Webcam Prediction** with bounding boxes and labels.
* ✅ **Easily Extendable Dataset** – add new people by storing their face data as `.npy` files.

---

## 🛠️ Tech Stack

* **Python 3.x**
* **NumPy** → handling dataset & distance calculations.
* **OpenCV** → face detection, image preprocessing, and real-time video capture.
* **KNN (custom implementation)** → classification of faces.


---

## 🚀 How it Works

1. **Dataset Creation**

   * Each person’s face images are stored as a `.npy` file.
   * Example: `AnvikaNegi.npy` → contains all face images of Anvika.
   * The dataset loader maps numeric IDs → names.

2. **Training (Data Preparation)**

   * `.npy` files are loaded and concatenated into:

     * `X` → feature matrix of flattened face images.
     * `y` → labels (numeric IDs for each person).

3. **KNN Algorithm**

   * For a new input face:

     * Compute distance from all training images.
     * Pick the top `k` nearest neighbors.
     * Assign the label by majority voting.

4. **Real-time Prediction**

   * Webcam captures a frame.
   * OpenCV detects face regions.
   * Each face is cropped, resized, and passed to KNN.
   * The predicted name is displayed on screen.

---

###  Run Real-time Recognition

Press **`q`** to quit the camera window.

---

## 📸 Example Output

* **Dataset loading**

```
AnvikaNegi.npy (34, 30000)
Gaurav.npy (55, 30000)
(89, 30000)
(89, 1)
{0: 'AnvikaNegi', 1: 'Gaurav'}
```

* **Live Webcam Prediction**
  Bounding box with predicted name:

```
[Face Detected] → Predicted: Gaurav
```

---

## 📌 Future Improvements

* 🔹 Improve face detection using DNN or MTCNN.
* 🔹 Add support for more robust classifiers (SVM, CNN).
* 🔹 Store embeddings instead of raw pixel intensities for better accuracy.

---

## 👨‍💻 Author

Developed by **Gaurav Singh** ✨
Contact -- officialgaurav0408@gmail.com
---

