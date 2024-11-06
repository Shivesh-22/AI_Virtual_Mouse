# AI_Virtual_Mouse
    An AI-driven virtual mouse program developed using OpenCV and Python. Using hand movements that are recognised by the computer's webcam, this program allows          hands-free mouse cursor control. To control mouse movements, it interfaces with PyAutoGUI and recognises gestures using a proprietary Hand_Tracking_Module.


Features

	•	Cursor Control: Move the cursor using the index finger.
	•	Left Click: Perform a left-click action by pinching with the index and middle fingers.
	•	Smooth Motion: Cursor movement is smoothed to provide a natural experience.
	•	On-screen Boundary Box: Helps to keep hand gestures within a defined frame for better control.


Requirements

	•	Python 3.x
	•	OpenCV (cv2)
	•	NumPy (numpy)
	•	PyAutoGUI
	•	Custom Hand_Tracking_Module
 
You can install the necessary packages using:

    pip install numpy
    pip install opencv
    pip install pyautogui


Installation

    1.	Clone this repository:
      git clone https://github.com/yourusername/AI-Virtual-Mouse.git
    2.	Navigate to the project directory:
      cd AI-Virtual-Mouse


Usage

	  1.	Ensure your webcam is connected.
	  2.	Run the virtual_mouse.py script:
   
        python virtual_mouse.py
        
    3.	The webcam will start, and a window named “Virtual Environment” will open.
	  4.	Control the cursor by moving your index finger. Make a “pinch” gesture (thumb and index finger together) to click.



Code Overview

Key Parameters

	•	wCam, hCam: Define the webcam resolution.
	•	frameR: Sets the frame boundary for gesture recognition to avoid accidental movements.
	•	smoothening: A factor to smooth the cursor movement.

Main Sections

	1.	Setup: Initialize the camera and required modules (htm for hand tracking, pyautogui for mouse control).
	2.	Hand Detection: Detect hand landmarks and retrieve positions of the index and middle fingers.
	3.	Gesture Recognition:
	•	Index Finger Only: Moves the cursor smoothly within the boundary box.
	•	Index and Middle Finger Together: Detects a “click” gesture.
	4.	FPS Display: Shows the frame rate in real time.
	5.	Display Output: Opens a window to visualize hand tracking and gesture detection.


How It Works

	1.	Hand Tracking: The Hand_Tracking_Module identifies hand landmarks using MediaPipe or a similar method.
	2.	Gesture Detection: By analyzing the positions of specific landmarks (index and middle finger tips), the program interprets gestures.
	3.	Mouse Control: Uses PyAutoGUI to translate gestures into mouse actions, including moving and clicking.


  Contributing

    Contributions are welcome! Please fork this repository, make your changes, and submit a pull request.
