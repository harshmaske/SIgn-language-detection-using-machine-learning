American-sign-language-detection-using-ML

Overview This project uses MediaPipe and OpenCV libraries to perform real-time pose detection and gesture classification from a video feed. The system detects and classifies hand gestures based on the angles between key landmarks on the face.

Libraries: cv2 (OpenCV) - for image processing and capturing video from the webcam. mediapipe - for detecting and analyzing poses. matplotlib - for plotting the landmarks in a 3D space. numpy - for mathematical operations and calculations. Features: Real-time pose detection using MediaPipe. Classification of hand gestures into categories like 'Fist' and 'Peace'. Visualization of detected landmarks and classifications. Installation Ensure you have the required libraries installed. You can install them using pip:

pip install opencv-python mediapipe matplotlib numpy

Usage: Initialize MediaPipe Pose: The mp_pose.Pose object is used to detect and track poses. Capture Video: Uses OpenCV to capture video from the default webcam. Process Frames: Each frame is processed to detect landmarks and classify gestures. Display Results: The detected landmarks and classifications are displayed on the video feed. Running the Code To run the code, execute the script:

python your_script_name.py The script will open a video window showing the webcam feed with detected landmarks and their classifications. Press 'q' to exit the video window.

Code Explanation Functions calculate_angle(a, b, c): Computes the angle between three points using the law of cosines. classify_sign(landmarks): Classifies hand gestures based on the angles between key points on the face. detect_poses(frame): Processes each frame to detect poses, classify gestures, and visualize the results. Main Execution The main section of the script sets up the video capture and continuously processes each frame using the detect_poses function. It will run until 'q' is pressed.

Notes Ensure your webcam is properly connected and accessible. Adjust MAX_ANGLE and MIN_ANGLE constants in the script to tune gesture classification if needed. The 3D scatter plot may not be visible in all environments; ensure matplotlib is properly configured to display or save plots.
