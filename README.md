# Object Detection and Distance Estimation with Audio Feedback

This project implements a real-time object detection and distance estimation system with audio feedback using YOLOv4-tiny, OpenCV, and Flask. The system detects various objects in a video stream, estimates their distance from the camera, and provides audio feedback about the detected objects and their distances.

## Project Overview

The main features of this project include:

1. Real-time object detection using YOLOv4-tiny
2. Distance estimation for detected objects
3. Audio feedback for detected objects and their distances
4. Web interface for viewing the video stream with detections

This system can be particularly useful for:
- Assisting visually impaired individuals in navigating their environment
- Enhancing situational awareness in various scenarios
- Educational purposes in computer vision and AI

## Prerequisites

- Python 3.7+
- Conda (for environment management)
- CUDA-capable GPU (for optimal performance)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/dhananjay6561/object-detection-distance-estimation.git
   cd StepSense
   ```

2. Create a Conda environment:
   ```bash
   conda create -n object_detection python=3.12
   conda activate object_detection
   ```

3. Install required packages:
   ```bash
   pip install opencv-python flask pyttsx3 numpy
   ```

4. Download YOLOv4-tiny weights:
   ```bash
   wget https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v4_pre/yolov4-tiny.weights
   ```

## Usage

1. Start the Flask application:
   ```bash
   python app.py
   ```

2. Open a web browser and navigate to `http://localhost:5000` to view the video stream with object detection and distance estimation.

## Project Structure

- `app.py`: Main application file containing object detection, distance estimation, and Flask server code
- `yolov4-tiny.cfg`: YOLOv4-tiny configuration file
- `classes.txt`: File containing class names for object detection
- `ReferenceImages/`: Directory containing reference images for distance calibration
- `templates/`: Directory containing HTML templates for the web interface

## How It Works

1. **Object Detection**: The system uses YOLOv4-tiny, a lightweight version of the YOLO (You Only Look Once) object detection algorithm, to detect objects in real-time from the video stream.

2. **Distance Estimation**: Distance is estimated using a focal length calculation based on known object sizes and their sizes in reference images. This allows the system to approximate the distance of detected objects from the camera.

3. **Audio Feedback**: The system uses pyttsx3 to provide audio feedback about detected objects and their estimated distances. The volume of the audio feedback is adjusted based on the estimated distance of the objects.

4. **Web Interface**: A Flask web server is used to stream the processed video with object detection bounding boxes and distance information to a web browser.

## Contributing

Contributions to improve the project are welcome! Here's how you can contribute:

1. Fork the repository
2. Create your feature branch:
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. Commit your changes:
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. Push to the branch:
   ```bash
   git push origin feature/AmazingFeature
   ```
5. Open a Pull Request

Areas for potential improvement:
- Enhancing distance estimation accuracy
- Adding support for more object types
- Improving the web interface
- Optimizing performance for lower-end devices

