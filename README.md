# Face Recognition System using OpenCV
This project implements a face recognition system using OpenCV. It leverages the haarcascade_frontalface_default.xml file to detect faces in images, crop them, and create a dataset for future predictions. The system also converts RGB images to grayscale to reduce complexity and improve performance.
Features
Detects faces in real-time using the Haar Cascade Classifier.
Converts RGB images to grayscale for simpler processing.
Extracts face coordinates using the detectMultiScale method.
Allows customization of parameters like scale factor and minimum neighbors for better accuracy.
Collects up to 200 face images or stops when the user presses the Enter key.



How It Works
Face Detection:
The Haar Cascade Classifier (haarcascade_frontalface_default.xml) is used to detect faces in an image.
The detectMultiScale method is employed to obtain face coordinates by passing parameters like:
Scale Factor: Determines how much the image size is reduced at each image scale.
Minimum Neighbors: Specifies how many neighbors each candidate rectangle should have to retain it. A higher value results in fewer detections but higher quality.

Grayscale Conversion:
RGB images are converted into grayscale, reducing complexity since grayscale images have only one channel compared to three in RGB.

Image Collection:

Detected faces are cropped and saved as individual images.
The process continues until 200 images are collected or the Enter key is pressed.
Dataset Creation:
The cropped face images are stored in a dataset folder for training and prediction purposes.
Technologies Used
Programming Language: Python
Library: OpenCV
Model: Haar Cascade Classifier (haarcascade_frontalface_default.xml)

Setup Instructions
Clone the repository:
bash
[git clone https://github.com/Ankitkumar9955/Face-Recognition-System.git](https://github.com/Ankitkumar9955/Face-Recognition-System)
cd face-recognition-opencv
Install the required dependencies:

bash
pip install opencv-python
pip install opencv-python-headless
Download the Haar Cascade XML file:

Ensure you have the haarcascade_frontalface_default.xml file in your project directory. You can download it from OpenCV GitHub.
Run the script:
bash
python face_recognition.py
Usage
Start the script, and it will open your webcam or process an input image (depending on your implementation).
The system will detect faces and crop them into individual images.
Images will be stored in a dataset folder for future use.

Parameters
You can experiment with the following parameters in the detectMultiScale method:

Parameter	Description
scaleFactor	Determines how much the image size is reduced at each image scale (e.g., 1.1).
minNeighbors	Specifies how many neighbors each candidate rectangle should have to retain it (e.g., 5).
Adjust these values based on your results for better detection accuracy.

Example Output
Detected faces are highlighted in real-time.
Cropped face images are saved in a designated folder as shown below:
dataset/
face_1.jpg
face_2.jpg........face_200.jpg


Future Improvements
Implement advanced models like CNNs for better accuracy.
Add support for real-time predictions using pre-trained models.
Integrate additional features like emotion detection or age estimation.

Contributing
Contributions are welcome! Feel free to fork this repository, make changes, and submit a pull request.

Acknowledgments
OpenCV library for providing powerful computer vision tools.
Haar Cascade Classifier for enabling efficient face detection.
