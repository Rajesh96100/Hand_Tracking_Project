Hand Tracking Project with OpenCV and Mediapipe
This project is a virtual painting application that allows users to draw on the screen using their fingers and select colors with hand gestures. The application uses OpenCV for object detection and the Mediapipe library for hand landmark detection.


#Usage
  To use the virtual painter, simply run the program and position your hand in front of the camera.
   The application will detect your hand and display 20 hand landmarks on the screen. You can use the following hand gestures to control the application:

->Two fingers up: Select color mode. Move your index finger to the desired color and use your other hand to make a fist to confirm your selection.
->One finger up: Drawing mode. Move your finger on the canvas to draw in the selected color.
->Two fingers down: Erase mode. Move your finger on the canvas to erase the drawing.

#Hand Tracking Module
  The Hand Tracking Module uses Mediapipe to detect hand landmarks in real-time. 
  The module crops the hand image from the webcam feed and uses computer vision preprocessing with the CV2 library to improve accuracy. 
  The findhands function is used to detect the hand in the image, and the findposition function returns the position of the hand landmarks. 
  The fingersUp function detects the number of fingers that are up.

# Gesture Hand Recognition Module
  The Gesture Hand Recognition Module uses the Hand Tracking Module to detect hand landmarks and recognize hand gestures.
  When two fingers are up and the hand position is less than 125 in the y direction, the selection mode is activated. In selection mode, 
  users can move their finger to select a color. When only one finger is up and the position is greater than 125 in the y direction, the drawing mode is activated. 
  In drawing mode, users can move their finger on the canvas to draw in the selected color.

# Acknowledgements
  This project would not have been possible without the following libraries and tools:
->OpenCV
->Mediapipe




