# Real-time Object Detection and Arduino Integration

This repository contains code for a real-time object detection system using YOLOv5, as well as an integration with an Arduino for sending detected object classes via serial communication.

## Prerequisites

Before running the code, make sure you have the following requirements installed:

- Python 3.x
- OpenCV (cv2) for webcam access
- PyTorch and YOLOv5 (required for object detection)
- PySerial for Arduino communication

## Installation

1. Clone the YOLOv5 repository:

   ```bash
   !git clone "https://github.com/ultralytics/yolov5.git"
   ```

2. Install required packages for YOLOv5:

   ```bash
   cd yolov5
   pip install -r requirements.txt
   ```

3. Start the webcam and perform real-time object detection:

   ```python
   python webcam_object_detection.py
   ```

## Real-time Object Detection

The `webcam_object_detection.py` script captures video from your webcam and performs object detection using a custom YOLOv5 model. Detected objects are labeled and displayed on the screen in real-time.

## Real-time Object Detection with Arduino Integration

The `webcam_object_detection_with_arduino.py` script extends the real-time object detection by integrating with an Arduino. Detected object classes are sent to the Arduino via serial communication.

### Arduino Setup

1. Connect your Arduino to your computer using a USB cable.

2. Upload the Arduino code (`arduino_code.ino`) provided in the repository to your Arduino.

3. Specify the correct serial port (`COMX` or `/dev/ttyX`) and baud rate (e.g., 9600) in the Python script.

4. Run the Python script:

   ```python
   python webcam_object_detection_with_arduino.py
   ```

   - Press 'q' to quit the script and close the webcam.
   - Press 'c' to close the webcam without quitting the script.

### Python Script Features

- Object detection using YOLOv5.
- Real-time webcam video feed.
- Object class labeling with bounding boxes.
- Sending detected object class to Arduino via serial communication.

## Customization

You can customize the script and YOLOv5 model to detect specific classes of objects. Modify the `classNames` list to match your desired object classes.

---

Feel free to modify and adapt this code to suit your specific project needs. Enjoy using the Real-time Object Detection and Arduino Integration system!
