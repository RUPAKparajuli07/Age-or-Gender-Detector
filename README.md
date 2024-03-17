## Documentation: Age and Gender Detection in Images

### Introduction
This Python script is designed to detect faces in images or via live webcam feed and predict the age and gender of the detected faces using deep learning models. It utilizes the OpenCV library to perform face detection and inference with pre-trained age and gender classification models.

### Features
- Detects faces in images or via live webcam feed.
- Predicts the age and gender of detected faces.
- Dynamically adjusts window size for display based on screen resolution.

### Libraries Used
- **OpenCV (cv2)**: OpenCV is a popular open-source computer vision library used for various image and video analysis tasks.
  - Installation command: `pip install opencv-python`

### Usage
1. **Command-line Arguments**:
   - `--image`: Path to the input image file. If not provided, the script will attempt to capture frames from the default webcam.

2. **Pre-trained Models**:
   - Face Detection Model:
     - **Files**: [opencv_face_detector.pbtxt](insert_drive_link_here), [opencv_face_detector_uint8.pb](insert_drive_link_here)
     - **Description**: Pre-trained deep learning model for face detection provided by OpenCV.
   - Age Estimation Model:
     - **Files**: [age_deploy.prototxt](insert_drive_link_here), [age_net.caffemodel](insert_drive_link_here)
     - **Description**: Pre-trained deep learning model for age estimation.
   - Gender Estimation Model:
     - **Files**: [gender_deploy.prototxt](insert_drive_link_here), [gender_net.caffemodel](insert_drive_link_here)
     - **Description**: Pre-trained deep learning model for gender estimation.

### Sharing Data
You can access the pre-trained models from Google Drive. Click on the following links to download the required files:
- [Face Detection Model](insert_drive_link_here)
- [Age Estimation Model](insert_drive_link_here)
- [Gender Estimation Model](insert_drive_link_here)

### Functionality
1. **Face Detection and Highlighting**:
   - The script utilizes the provided face detection model to detect faces in the input image or video frames.
   - Detected faces are highlighted with bounding boxes on the processed image.

2. **Age and Gender Estimation**:
   - For each detected face, the script extracts the face region and predicts its age and gender.
   - Age and gender predictions are displayed on the processed image along with the bounding box.

3. **Dynamic Window Adjustment**:
   - The script dynamically adjusts the size of the output window based on the screen resolution for optimal display.

### Running the Script
1. Ensure that the required libraries are installed, especially OpenCV (`opencv-python`).
2. Download the pre-trained models from the provided Google Drive links and place them in the same directory as the script.
3. Run the script with appropriate command-line arguments:
   ```
   python script_name.py --image path/to/input_image.jpg
   ```
   Replace `script_name.py` with the actual name of the Python script.

4. Alternatively, if no image path is provided, the script will attempt to capture frames from the default webcam.

### Dependencies
- Python 3.x
- OpenCV (cv2)
- Pre-trained models: face detection model, age estimation model, gender estimation model

### References
- OpenCV documentation: [https://docs.opencv.org/](https://docs.opencv.org/)
- Caffe Model Zoo: [https://github.com/BVLC/caffe/wiki/Model-Zoo](https://github.com/BVLC/caffe/wiki/Model-Zoo)

### Note
- Ensure that the input image or video frames contain clear and visible faces for accurate detection and estimation results.
