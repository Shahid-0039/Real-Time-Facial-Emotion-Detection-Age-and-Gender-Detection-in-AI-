# Real-Time Facial Emotion, Age, and Gender Detection in AI

## Project Overview

This project provides a real-time system for detecting facial emotions, age, and gender from webcam/video input using deep learning and computer vision techniques. The system utilizes pre-trained models to recognize emotions, estimate age groups, and identify gender from detected faces, displaying the results live on the video feed.

## Features

- **Real-Time Detection:** Processes live webcam feeds to detect faces and analyze them instantly.
- **Emotion Recognition:** Classifies emotions such as Angry, Disgust, Fear, Happy, Sad, Surprise, and Neutral.
- **Age Estimation:** Predicts age groups such as (0-2), (4-6), (8-12), (15-20), (20-30), (30-40), (40-55), and (60-100).
- **Gender Classification:** Identifies gender as Male or Female.
- **Visualization:** Draws bounding boxes and overlays detected attributes (emotion, age, gender) on the video frames.

## Technologies Used

- **Python**
- **OpenCV** - For video capture, face detection, and visualization.
- **TensorFlow/Keras** - For loading and running the emotion detection model.
- **Caffe** - For running pre-trained age and gender detection models.
- **NumPy & Matplotlib** - For data handling and visualization.

## How It Works

1. **Face Detection:** Uses OpenCV's Haar Cascade classifier to detect faces in each video frame.
2. **Emotion Detection:** Preprocesses the face and predicts the emotion using a Keras model (`emotion_detection_model.h5`).
3. **Age & Gender Detection:** Uses OpenCV DNN module to run Caffe models (`age_net.caffemodel`, `gender_net.caffemodel`).
4. **Result Visualization:** Draws rectangles around faces and overlays labels for emotion, age, and gender.

## Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Shahid-0039/Real-Time-Facial-Emotion-Detection-Age-and-Gender-Detection-in-AI-.git
   cd Real-Time-Facial-Emotion-Detection-Age-and-Gender-Detection-in-AI-
   ```

2. **Install Dependencies**
   Make sure you have Python 3.x installed. Then install the required libraries:
   ```bash
   pip install opencv-python tensorflow numpy matplotlib
   ```

3. **Download Pre-trained Models**
   - Place your emotion detection model (`emotion_detection_model.h5`) in the project directory.
   - Place the Caffe model files (`age_deploy.prototxt`, `age_net.caffemodel`, `gender_deploy.prototxt`, `gender_net.caffemodel`) in the specified paths or update the code to your paths.

## Usage

1. **Run the Notebook**
   Open and run the Jupyter notebook:  
   `Project of AI/Face Emotion, Gender and Age Detection .ipynb`

2. **Live Detection**
   The notebook will access your webcam and display a live window with results. Press `q` to exit.

   - Each detected face will show:
     - **Emotion:** (e.g., Happy, Sad, etc.)
     - **Gender:** (Male/Female)
     - **Age Group:** (e.g., 15-20)

## Example

![Example Screenshot](example_screenshot.png)  
*Live detection showing overlays for emotion, age, and gender.*

## Notes

- The models must be downloaded separately due to their size and licensing.
- Ensure your webcam is connected and accessible.
- Paths to model files may need to be adjusted based on your environment.

## Credits

Developed by Shahid-0039.  
Uses open-source models and libraries from the AI and computer vision community.

## License

This project is for educational and research purposes. See the repository for license details.
