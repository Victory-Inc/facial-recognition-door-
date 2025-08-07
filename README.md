# AI Face Recognition Security System

## Description

This project consists of a circuit that utilizes a Raspberry Pi, a webcam, and a trained AI algorithm to detect faces. The system determines whether the detected face is approved (authorized) or a foreign face (unauthorized). When an unauthorized face is detected, the system can trigger various outputs including a buzzer, RGB LED alert, and a locking mechanism driven by a serial motor. The system can also be armed or disarmed using a button.

## Parts Used

- 1 × RGB LED  
- 1 × Piezo Buzzer  
- 1 × Button  
- 1 × Serial Motor  
- 1 × Raspberry Pi  
- 1 × USB Webcam  

## How It Works

1. **Face Detection:**  
   The webcam captures video input, which is analyzed by a facial recognition AI model running on the Raspberry Pi.

2. **Recognition:**  
   - If the face is recognized as an approved face, the RGB LED may turn green, and no action is taken.  
   - If the face is not recognized (unauthorized), the RGB LED turns red, the buzzer sounds an alert, and the motor locks a connected mechanism.

3. **Arming/Disarming:**  
   A button is used to toggle the system between armed and disarmed states. The system only responds to face detection when it is armed.

## Setup Overview

1. Train your AI model with approved faces using a library like OpenCV or `face_recognition` in Python.
2. Connect your components to the Raspberry Pi:
   - RGB LED to GPIO (with resistors)
   - Piezo buzzer to GPIO
   - Button to GPIO with pull-down resistor
   - Serial motor to appropriate driver or shield controlled by GPIO
   - Webcam via USB
3. Deploy and run your Python script for detection and response logic.
