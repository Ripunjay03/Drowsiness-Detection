# Real-Time Drowsiness Detection System

## Features
- Detects drowsiness by monitoring eye aspect ratio (EAR) using webcam.
- Detects yawning by measuring lip distance.
- Plays an alert sound when drowsiness or yawning is detected.
- Uses computer vision techniques with OpenCV and dlib.
- Real-time video stream processing from webcam.

## How Drowsiness Detection Works
This project detects drowsiness by calculating the Eye Aspect Ratio (EAR) from the user's eye landmarks detected in the webcam video stream. The EAR is a measure of the openness of the eyes. When the EAR falls below a certain threshold for a consecutive number of frames, it indicates that the eyes are closed or nearly closed, signaling drowsiness. An alert sound is played to warn the user.

Similarly, yawning is detected by measuring the distance between the upper and lower lips. If the lip distance exceeds a threshold, a yawn alert is triggered.

## Technologies Used
- Python 3
- OpenCV for computer vision and image processing
- dlib for facial landmark detection
- imutils for image processing convenience functions
- numpy for numerical operations
- playsound for playing alert sounds
- scipy for scientific computing

## Uses
- Can be used by drivers to prevent accidents caused by drowsiness.
- Useful for monitoring alertness in various safety-critical environments.
- Can be adapted for research or educational purposes in computer vision and machine learning.

## Installation
1. Ensure you have Python 3.6 or higher installed.
2. Clone or download this repository.
3. Open a terminal in the project directory.
4. Install the required Python packages by running:
   ```
   pip install -r requirements.txt
   ```
5. Make sure the following files are present in the project directory:
   - `drowsiness_yawn.py`
   - `Alert.wav`
   - `haarcascade_frontalface_default.xml`
   - `shape_predictor_68_face_landmarks.dat`

## How to Run
After installing the dependencies, run the project using the following command:
```
python drowsiness_yawn.py --webcam 0 --alarm Alert.wav
```
- `--webcam` specifies the index of the webcam to use (default is 0).
- `--alarm` specifies the path to the alert sound file.

Press `q` to quit the program at any time.

## Notes
After installing the dependencies, run the project using the following command:
- The default alarm sound file is `Alert.wav` located in the project directory.
- Adjust the webcam index if you have multiple cameras connected.
- Ensure your webcam is accessible and not used by other applications.
