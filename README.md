# Documentation

This project utilizes [YOLOv5](https://github.com/ultralytics/yolov5), a state-of-the-art real-time object detection system, for controlling a car in a game using hand gestures. The YOLOv5 model is trained on custom dataset for controlling the car movements. 
 
# WORKING

The YOLOv5 system detects hand gestures in real-time. Once a gesture is recognized, the system simulates pressing the relevant key on the keyboard to control the car's movement in the game. For example, if the YOLOv5 system detects a "mvefrd" gesture, it simulates pressing the "W" key to move the car forward.  

Below are the steps to install, run, and use the system: 

## Install

1. Clone the repository and navigate to the project directory:

    ```bash
    git clone https://github.com/bilal77511/yolov5-hand-gesture-car-game-control.git  # clone
    cd yolov5
    ```

2. Install the required dependencies by running the following command:

    ```bash
    pip install -r requirements.txt  # install
    ```

3. Ensure that you are using a Python environment with version 3.8.0 or higher and have PyTorch installed (version 1.8.0 or later).

## Run

4. Run the detection script with the desired configuration:

    ```bash
    python detectnew.py --weights RESULTS/weights/best.pt --img 640 --conf 0.25 --source 0  # running
    ```

    This command will use the trained YOLOv5 model to detect hand gestures in real-time.

6. Now, open the car game that you want to play. The hand gestures detected by YOLOv5 will be translated into corresponding game controls, allowing you to interact with the game using your hand movements.

## Gesture Controls

The system is designed to recognize four gestures that are mapped to control the car movements in the game:
![Gesture Controls](https://raw.githubusercontent.com/bilal77511/yolov5-hand-gesture-car-game-control/master/RESULTS/GESTURES.jpg)

- **1:** Steer the car to the left.
- **2:** Move the car forward.
- **3:** Move the car backward.
- **4:** Steer the car to the right.  
  You can watch the [demo](https://youtu.be/nolA7gAj25A) to understand the controls better.

## Issues and Bugs
### Issue: Dual-Hand Control

One limitation encountered during the development was the difficulty in implementing dual-hand control for the car. The initial goal was to enable users to use both hands to control different aspects of the car's movements. However, due to technical constraints or specific challenges, achieving this functionality proved challenging.

### Lattency

Another challenge faced during the development of the project was latency. The system experienced delays in detecting and responding to hand gestures, impacting the real-time responsiveness expected in a gaming environment.

### Bugs: Control Stuck and Continuous Movement

A notable bug observed during testing was the occasional occurrence of control getting stuck, leading to continuous movement of the car even when the user's hand gestures indicated a stop or a change in direction. This unexpected behavior needs further investigation and debugging to ensure a smoother and more reliable gaming experience.

## YOLOv5 Training Details

The YOLOv5 model used in this project is trained on custom dataset to ensure accurate detection of hand gestures. The [training results](https://github.com/bilal77511/yolov5-hand-gesture-car-game-control/tree/e82314435a1e12c03a5fa2f5631b5c62c4aa4285/RESULTS) indicate good accuracy, and the model is capable of real-time inference for controlling the car in the game.

For more detailed information and customization options, refer to the [YOLOv5 Documentation](https://docs.ultralytics.com/yolov5/).

Feel free to explore and adapt the project based on your preferences and specific game requirements.
