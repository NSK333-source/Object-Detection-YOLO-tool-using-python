# Object-Detection-YOLO-tool-using-python
This is a YOLO based python object detection tool 

This Python script demonstrates real-time object detection using the MobileNet SSD (Single Shot MultiBox Detector) model. Here’s a breakdown of its functionality:

Imports and Initialization:
The script imports necessary packages such as VideoStream, FPS, numpy, argparse, imutils, time, and cv2.
It initializes the list of class labels that the MobileNet SSD model can detect and generates random bounding box colors for each class.
Model Loading:
The MobileNet SSD model is loaded from disk using cv2.dnn.readNetFromCaffe().
The pre-trained model consists of a prototxt file (MobileNetSSD_deploy.prototxt.txt) and a binary model file (MobileNetSSD_deploy.caffemodel).
Video Stream and FPS Counter:
The script initializes the video stream from the default camera (webcam).
It allows the camera sensor to warm up for 2 seconds.
An FPS counter is started to measure the frame rate.
Main Loop:
The script continuously captures frames from the video stream.
Each frame is resized to a maximum width of 400 pixels using imutils.resize().
A blob is created from the resized frame for input to the neural network.
Object Detection and Visualization:
The blob is passed through the network, and detections are obtained.
For each detection:
The confidence (probability) associated with the prediction is extracted.
Weak detections (confidence below 20%) are filtered out.
The class label index is determined, and bounding box coordinates are computed.
The bounding box and label are drawn on the frame.
The detected object’s label and confidence are displayed.
The processed frame is shown in a window using cv2.imshow().
User Interaction:
The script listens for the ‘q’ key press. If pressed, it breaks out of the loop.
FPS Calculation and Cleanup:
The FPS timer is stopped, and elapsed time and approximate FPS are displayed.
The OpenCV window is closed, and the video stream is released.
Overall, this script provides a real-time object detection experience using the MobileNet SSD model. Objects are identified, and bounding boxes with labels are overlaid on the video stream. Feel free to customize the confidence threshold and explore different classes! 😊



 Real-time object detection with deep learning and OpenCV

Installation:
- `pip install numpy`
- `pip install opencv-python`
- `pip install imutils`

To Run the project:

- `python real_time_object_detection.py`
