# Hand Gesture-Based Control System
This project uses OpenCV, Mediapipe, and PyAutoGUI to recognize hand gestures via a webcam and perform actions like adjusting system volume, changing screen brightness, and switching between applications.

## Features
* **Volume Control:** Adjust system volume based on the distance between specific hand landmarks.
* **Brightness Control:** Control screen brightness using hand gestures.
* **Application Switcher:** Switch between applications (Alt + Tab) with a pinch gesture.
## Project Structure
* **hand_gesture_control.py:** The main Python script that uses the webcam to detect hand gestures and perform actions accordingly.
* **README.md:** This file providing an overview of the project.
## Prerequisites
Before running the project, ensure you have the following installed:

* Python 3.x
* OpenCV (cv2)
* Mediapipe
* PyAutoGUI
* Screen Brightness Control (for brightness adjustment)
You can install these libraries using the following command:

```bash

pip install opencv-python mediapipe pyautogui screen-brightness-control
```
## How It Works
**Landmark Detection:** The script uses Mediapipe to detect hand landmarks. Based on the relative positions of key points (fingers), the script performs various system actions.
* **Volume Control:** The distance between the thumb tip and the pinky finger tip controls the system volume (increase or decrease).
* **Brightness Control:** The distance between the index finger and thumb is used to control screen brightness.
* **App Switch:** A pinch gesture between the index finger and thumb allows you to switch between open applications using the Alt + Tab combination.
## Running the Project
1. Clone this repository:

```bash
git clone https://github.com/username/hand-gesture-control.git
```
2. Navigate to the project directory:

```bash

cd hand-gesture-control
```
3. Run the Python script:
```bash

python hand_gesture_control.py
```
4. Press ESC to exit the program.

 ## Key Functions
* **cv2.VideoCapture(0):** Opens the webcam.
* **Mediapipe Hands:** Detects hand landmarks and tracks finger movements.
* **pyautogui.press():** Simulates key presses (for volume control and app switching).
* **svc.set_brightness():** Adjusts screen brightness based on gesture.
## Hand Gestures
* **Volume Control:** When the distance between the thumb tip and pinky tip increases, volume is increased. When the distance decreases, the volume is lowered.

* **Brightness Control:** The distance between the index finger tip and thumb tip is used to adjust brightness.

* **App Switch:** A pinch gesture between the index finger and thumb switches between open applications (Alt + Tab).

## Notes
* The project is designed for use with a webcam (default is cv2.VideoCapture(0)).
* Ensure your system allows for programmatic volume and brightness control.
