# Hand Detection Model using OpenCV

### Project Overview
This code is a program that uses computer vision and machine learning to detect hands in real-time video feed and draw a landmark on each hand joint.

##### Libraries and versions used
Library         | Version | Installation Command
--------------- | ------- | --------------------
Python          | 3.x     | -
OpenCV-Python   | 4.x     | pip install opencv-python
MediaPipe     | 0.9.1   | pip install mediapipe
Imutils       | 0.5.4  | pip install imutils

### Running the script
1. Clone the repository to your local machine
    ```bash
    git clone https://github.com/Nicolas-Formenton/Hand_Detection_Model_ML.git
    ```
2. Change into the directory of the cloned repository
    ```bash 
    cd Hand_detection_Model_ML
    ```
3. Install the required libraries
    ```bash
    python -m pip install -r requirements.txt
    ```
4. Have Jupyter Notebook installed and then run the cells you want to test.

### Code Explanation
The code is written in Python and uses the following libraries:

Library         | Usage   |
--------------- | ------- | 
OpenCV          | Used for image processing tasks, such as converting the image to grayscale and applying thresholding.| 
MediaPipe |  Framework for building multi-modal applied machine learning pipelines. It enables quick and easy prototyping and deployment of computer vision and machine learning models.
Imutils | Provides a simple and intuitive API that makes it easier to perform common image processing tasks in computer vision projects

The code is a hand tracking program using OpenCV, MediaPipe, and imutils. The code captures video from the default camera and processes each frame to detect hands and landmarks in the image. It uses MediaPipe to process the hand landmarks, including the connections between the landmarks. imutils is used to resize the video frames to a specific size for processing.

The code also displays the number of hands detected in the image and the frames per second (FPS) of the video capture on the output image. It continues to process frames until the user presses the 'q' key, which will close the video capture and the program.

The code uses the OpenCV VideoCapture class to access the video stream from the camera. The frames are read in a loop and processed using the process_image and draw_hand_connections functions. The process_image function uses MediaPipe to process the image and detect hand landmarks, while the draw_hand_connections function uses MediaPipe and OpenCV to draw the hand landmarks and connections on the image.

The code also calculates the FPS of the video stream using a combination of the time module and frame counting. The FPS is displayed on the output image using the OpenCV putText function, which writes text on the image.