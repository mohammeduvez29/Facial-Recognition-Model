# Face Recognition with OpenCV and Face Recognition Library

This project demonstrates real-time face recognition using OpenCV and the `face_recognition` library. The system detects faces from a live camera feed and identifies them based on pre-encoded images.

## Features
- Detects faces from live video feed.
- Recognizes known faces based on pre-encoded images.
- Highlights identified faces with bounding boxes and names.

## Prerequisites

### Software Requirements
- Python 3.6 or higher
- OpenCV
- face_recognition library
- NumPy

### Hardware Requirements
- A working webcam for real-time face detection.

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/your_username/face-recognition-opencv.git
   cd face-recognition-opencv
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Ensure you have a folder named `images/` in the root directory of the project. Add images of known faces to this folder. Name the images with the corresponding person's name (e.g., `john_doe.jpg`).

## Usage
1. Run the script:
   ```bash
   python face_recognition.py
   ```
2. The system will access your webcam, detect faces, and identify known ones.
3. Press `ESC` to exit the program.

## Project Structure
```
.
├── face_recognition.py     # Main script for real-time face recognition
├── simple_facerec.py       # Helper class for face encoding and recognition
├── images/                 # Folder containing known face images
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

## Code Explanation

### face_recognition.py
This script initializes the camera feed, loads encoded images, and performs face detection and recognition in real-time.

### simple_facerec.py
This class encapsulates methods to:
- Load and encode images from the `images/` directory.
- Detect and identify faces from frames using the `face_recognition` library.

## Example Output
- Recognized faces will be highlighted with a rectangle and their name displayed below the rectangle.
- Unknown faces will be labeled as "Unknown".

### Output Image Example
Here is an example of the face recognition output:

![Face Recognition Output](images/output_example.jpg)

## Dependencies
Add the following libraries to your `requirements.txt` file:
```
opencv-python
face_recognition
numpy
```

## Troubleshooting
- **Error: ModuleNotFoundError: No module named 'face_recognition'**
  Ensure you have installed the `face_recognition` library. On some systems, you may need to install `dlib` before installing `face_recognition`:
  ```bash
  pip install dlib
  pip install face_recognition
  ```
- **Error: Camera not working**
  Check your webcam permissions or ensure it is properly connected.

## License
This project is open-source and available under the MIT License.

## Acknowledgments
- [OpenCV](https://opencv.org/) for real-time image processing.
- [face_recognition](https://github.com/ageitgey/face_recognition) library for face detection and recognition.

## Contribution
Feel free to fork this repository and submit pull requests to improve the functionality or fix bugs.
