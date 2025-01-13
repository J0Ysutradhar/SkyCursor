# SkyCursor
The Virtual Mouse Using Hand Gestures project enables users to control their computer mouse with simple hand movements captured via a webcam
## Virtual Mouse Using Hand Gestures

This Python project leverages computer vision and gesture recognition to control the mouse pointer using hand gestures. The program uses the Mediapipe library to detect hand landmarks and PyAutoGUI to interact with the mouse pointer.
## Features
- **Hand Detection**: Detects the position of the hand and fingers in real-time.
- **Mouse Movement**: Moves the mouse pointer according to the index finger's position.
- **Click Detection**: Performs a mouse click when the index finger and thumb come close together.

## Prerequisites

1. Python 3.x installed on your system.
2. The following libraries must be installed:
   - OpenCV
   - Mediapipe
   - PyAutoGUI

Install them using:
```bash
pip install opencv-python mediapipe pyautogui
```

## How It Works

1. The webcam captures video frames in real-time.
2. Mediapipe processes the video frames to detect hand landmarks.
3. The index finger's position is mapped to the screen dimensions to control the mouse pointer.
4. When the thumb and index finger come close, a click event is triggered.

## Usage

### Step 1: Run the Program
Execute the script using:
```bash
python main.py
```

### Step 2: Interact with the Virtual Mouse
- **Move the Pointer**: Point with your index finger. The pointer will follow its movements.
- **Click**: Bring your thumb and index finger close together to perform a click.

### Notes
- Ensure good lighting and proper visibility of your hand for accurate detection.
- The screen resolution is automatically detected, but you can adjust the scaling factors (`index_x` and `index_y` calculation) if needed.

## Customization

- **Sensitivity**: Modify the sensitivity for click detection by changing this threshold in the code:
  ```python
  if abs(index_y - thumb_y) < 18:
  ```
- **Frame Display**: The program displays a live feed with landmarks drawn on the detected hands. You can remove the visualization by commenting out this line:
  ```python
  drawing_utils.draw_landmarks(frame, hand)
  ```

## Limitations

- The program requires a clear and unobstructed view of the hand.
- Performance may vary depending on the webcam quality and lighting conditions.

## Dependencies

The following libraries are required:
- `opencv-python`
- `mediapipe`
- `pyautogui`

Install them using the command mentioned in the prerequisites.

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute this script.
