# Smart Face Recognition System with Unknown Face Detection

This repository contains a Python-based project that implements a real-time face recognition system using **OpenCV** and **DeepFace** for advanced facial recognition and management of unknown individuals. 

## Features
- **Face Recognition**: Identifies known individuals using pre-trained DeepFace models.
- **Unknown Face Detection**: Detects and handles unrecognized faces by saving their images after a timeout period.
- **Real-Time Processing**: Captures and processes video feed from the webcam in real-time.
- **Dynamic Actions**: Labels recognized faces and triggers alerts or actions for unknown faces.

## How It Works
1. The system loads known face images and their respective names from the specified paths.
2. Captures video frames from the webcam.
3. Uses OpenCV's Haar Cascade to detect faces in the video stream.
4. Compares the detected face with known face images using DeepFace.
5. If a match is found:
   - Labels the face with the corresponding name.
6. If the face is unknown:
   - Starts a 7-second timer.
   - Saves the image of the unknown face locally if it remains unidentified for 7 seconds.
7. Displays the video feed with labeled faces and bounding boxes.

## Prerequisites
Make sure you have the following installed:
- Python 3.x
- Required Python libraries:
  ```
  pip install opencv-python deepface
  ```

## File Structure
- **face_recognition_system.py**: Main script for the face recognition system.
- **Images Folder**: Directory containing images of known individuals.
- **temp_face.jpg**: Temporary file for processing detected faces.

## Usage
1. Clone this repository:
   ```
   git clone https://github.com/ChaitanyaShirse/Smart-Face-Recognition-System.git
   ```
2. Navigate to the project directory:
   ```
   cd Smart-Face-Recognition-System
   ```
3. Update the script:
   - Modify the `image_paths` variable to include paths to your known face images.
   - Update the `known_face_names` variable with the corresponding names.
4. Run the script:
   ```
   python face_recognition_system.py
   ```
5. Press `q` to exit the application.

## Future Enhancements
- **Email Notification**: Send alerts to cardholders with the captured unknown face image.
- **Cloud Integration**: Store and analyze face data securely on the cloud.

## Screenshots
- **Real-Time Face Recognition**:
  ![Screenshot Example](example_screenshot.jpg)
- **Unknown Face Detection**:
  ![Unknown Face Example](unknown_face_screenshot.jpg)

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
- [DeepFace](https://github.com/serengil/deepface): Python library for facial recognition.
- [OpenCV](https://opencv.org/): Open-source computer vision library.

---

Thank you for checking out this project! Contributions are welcome. Feel free to fork this repository and submit a pull request.
