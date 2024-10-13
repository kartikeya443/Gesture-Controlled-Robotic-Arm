# Gesture-Controlled Robotic Arm

This project implements a gesture-controlled robotic arm using computer vision and hand tracking technologies. It allows users to intuitively control a 4-DOF (Degrees of Freedom) robotic arm using hand movements captured by a camera.

## Features

- Real-time hand tracking and gesture recognition using MediaPipe and OpenCV
- Control of 4 servo motors (X, Y, Z axes and gripper) based on hand gestures
- Intuitive mapping of hand movements to robotic arm actions:
  - X-axis: Controlled by the angle between wrist and index finger
  - Y-axis: Controlled by the vertical position of the wrist
  - Z-axis: Controlled by the size of the palm (distance from camera)
  - Gripper: Opens or closes based on open hand or fist gesture
- Serial communication to interface with an Arduino-controlled robotic arm
- Real-time visualization of hand tracking and servo angles
- Configurable parameters for fine-tuning gesture recognition and servo mappings

## Technologies Used

- Python
- OpenCV
- MediaPipe
- PySerial
- Arduino

## Applications

This project has potential applications in:

- Remote manipulation in hazardous environments
- Assistive technology for individuals with limited mobility
- Industrial automation and human-robot interaction
- Educational tools for robotics and programming
- Virtual reality and telepresence systems

## Hand Landmarks

<img width="1073" alt="hand-landmarks" src="https://github.com/user-attachments/assets/b3546ba2-ade8-4a44-bd2e-eeed9f05bec0">

## Arduino Architecture

![arduino_archi](https://github.com/user-attachments/assets/15ab100f-df04-4087-9582-b1e3e42042f0)

## Getting Started

### Prerequisites

- Python 3.7 or higher
- Arduino IDE
- USB camera or IP camera
- 4-DOF robotic arm with servo motors

### Installation

1. Install Python dependencies:
   ```
   pip install -r requirements.txt
   ```

2. Upload Arduino sketch:
   - Open `ard_main.ino` in the Arduino IDE
   - Connect your Arduino board
   - Select the correct board and port in the Arduino IDE
   - Upload the sketch to your Arduino

3. Configure the Python script:
   - Open `cv_main.py`
   - Adjust the `cam_source` variable to match your camera setup
   - Modify the `ser` variable to match your Arduino's serial port

4. Run the Python script:
   ```
   python cv_main.py
   ```

5. Position your hand in front of the camera and start controlling the robotic arm with your gestures!

## Configuration

You can adjust various parameters in `cv_main.py` to fine-tune the gesture recognition and servo mappings. Refer to the comments in the code for details on each parameter.

## Future Improvements

- [ ] Add support for multiple hand gestures
- [ ] Implement machine learning for more complex gesture recognition
- [ ] Develop a graphical user interface for easy calibration

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
