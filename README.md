# Real-Time Face Recognition using KNN and OpenCV

A real-time computer vision project that detects and recognizes faces from a webcam feed using OpenCV and a custom K-Nearest Neighbors (KNN) classifier.

## Title

**Real-Time Face Recognition System (OpenCV + KNN)**

## Key Highlights

- Built an end-to-end face recognition pipeline from data collection to live prediction.
- Implemented KNN classification logic from scratch (without scikit-learn).
- Used Haar Cascade-based face detection for real-time webcam inference.
- Designed a simple extensible dataset workflow using `.npy` files per identity.

## Tech Stack

- Python
- NumPy
- OpenCV
- KNN (custom implementation)

## Project Structure

- `FaceRecognition_KNN/faceDataCollect.ipynb` - captures and stores face samples.
- `FaceRecognition_KNN/faceRecognition.ipynb` - performs training and live recognition.
- `FaceRecognition_KNN/K_Nearest_Neigbours_Classifications.ipynb` - KNN workflow notebook.
- `FaceRecognition_KNN/haarcascade_frontalface_alt.xml` - face detection model.
- `requirements.txt` - Python dependencies.

## How It Works

1. Collect face samples from webcam input and store them as `.npy` files.
2. Load and flatten face arrays to build feature matrix (`X`) and label vector (`y`).
3. Predict identity using nearest-neighbor voting on Euclidean distance.
4. Display live webcam frames with bounding boxes and predicted names.

## Setup

```bash
git clone https://github.com/GauravSingh0248/face-recognition.git
cd face-recognition
python -m venv venv
# Windows
venv\Scripts\activate
pip install -r requirements.txt
```

## Run

Open and run notebooks in this order:

1. `FaceRecognition_KNN/faceDataCollect.ipynb`
2. `FaceRecognition_KNN/faceRecognition.ipynb`

## Future Enhancements

- Improve detection robustness with DNN/MTCNN-based detectors.
- Replace raw pixels with face embeddings for better accuracy.
- Add model evaluation metrics and confusion matrix reporting.

