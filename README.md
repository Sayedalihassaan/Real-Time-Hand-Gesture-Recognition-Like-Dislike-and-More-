## Real-Time Hand Gesture Recognition (Like, Dislike, and More)
This project implements a real-time hand gesture recognition system using MediaPipe and OpenCV. It detects hand gestures such as "Like," "Dislike," "Stop," "Forward," "Backward," "Left," and "Right" from webcam input, overlaying corresponding icons and text labels on the video feed. The project is built using Python and is ideal for applications in human-computer interaction.

## Table of Contents

Project Overview
Features
Requirements
Installation
Usage
Project Structure
Gesture Details
Contributing
License
Acknowledgements

## Project Overview
The Real-Time Hand Gesture Recognition project uses MediaPipe's hand tracking module to detect and analyze hand landmarks from a webcam feed. It identifies specific hand gestures by analyzing the positions of fingertips and the thumb, displaying the gesture name and an optional icon (e.g., thumbs-up for "Like"). The system is designed for real-time performance and can be extended to control applications or devices based on gestures.
Features

Real-time hand gesture detection using MediaPipe.
Recognition of multiple gestures: Like, Dislike, Stop, Forward, Backward, Left, Right.
Visual feedback with text labels and gesture-specific icons.
Hand landmark visualization with colored markers and connections.
Customizable webcam input resolution.
Easy-to-use Python script with OpenCV for video processing.

Requirements
To run this project, you need the following:

Python 3.11 or higher
A webcam (built-in or external)
Image files for "Like" and "Dislike" gestures (like.png, dislike.png)

Python Libraries

opencv-python
mediapipe
numpy

Installation
Follow these steps to set up the project locally:

Clone the Repository
git clone https://github.com/your-username/hand-gesture-recognition.git
cd hand-gesture-recognition


Set Up a Virtual Environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate


Install Dependencies
pip install -r requirements.txt


Prepare Gesture Icons

Place like.png and dislike.png in an images/ directory within the project root.
Alternatively, update the image paths in the script to match your file locations.


Ensure Webcam Access

Verify that your webcam is functional and accessible by OpenCV.



Usage

Ensure the images/ directory contains like.png and dislike.png, or update the paths in the script.
Run the gesture recognition script:python gesture_recognition.py


The script will:
Open the webcam and process video frames in real-time.
Detect hand gestures and display the gesture name (e.g., "LIKE", "STOP") on the video.
Overlay gesture-specific icons for "Like" and "Dislike".
Draw hand landmarks with colored circles and lines.


Perform gestures in front of the webcam to see the results.
Press q to exit the application.

Example Output
The output window displays the webcam feed with:

Red text labels indicating the detected gesture (e.g., "LIKE", "STOP").
Thumbs-up/down icons for "Like" and "Dislike" gestures.
Blue circles on fingertip landmarks and green lines connecting hand landmarks.
Console output of detected gestures for debugging.

Project Structure
hand-gesture-recognition/
├── images/
│   ├── like.png              # Icon for Like gesture
│   ├── dislike.png           # Icon for Dislike gesture
├── gesture_recognition.py    # Main script for gesture recognition
├── Like and Dislike.ipynb    # Jupyter notebook with the code
├── requirements.txt          # List of Python dependencies
├── README.md                 # Project documentation

Gesture Details
The system recognizes the following gestures based on hand landmark positions:

Like: All fingers folded, thumb pointing upward.
Dislike: All fingers folded, thumb pointing downward.
Stop: All fingers extended, palm facing the camera.
Forward: Thumb extended right, index finger up, others folded.
Backward: Thumb extended left, middle, ring, and pinky fingers up.
Left: Thumb and index finger extended, others folded, palm facing left.
Right: Thumb and index finger extended, others folded, palm facing right.

Gestures are detected by comparing the x and y coordinates of specific landmarks (e.g., fingertips, thumb tip).
Contributing
Contributions are welcome! To contribute:

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes and commit (git commit -m "Add feature").
Push to the branch (git push origin feature-branch).
Open a Pull Request.

Please ensure your code follows the project's coding style and includes relevant tests.
License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgements

MediaPipe for hand tracking and landmark detection.
OpenCV for video processing and visualization.
Inspiration from real-time computer vision applications.

For any questions or issues, please open an issue on the GitHub repository.
