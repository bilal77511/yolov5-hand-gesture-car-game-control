# Documentation

This project utilizes [YOLOv5](https://github.com/ultralytics/yolov5), a state-of-the-art real-time object detection system, for controlling a car in a game using hand gestures. The YOLOv5 model is trained on custom dataset for controlling the car movements. Below are the steps to install, run, and use the system:

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

- **Forward (W):** Move the car forward.
- **Left (A):** Steer the car to the left.
- **Backward (S):** Move the car backward.
- **Right (D):** Steer the car to the right.

## YOLOv5 Training Details

The YOLOv5 model used in this project is trained on custom data to ensure accurate detection of hand gestures. The training results indicate good accuracy, and the model is capable of real-time inference for controlling the car in the game.

For more detailed information and customization options, refer to the [YOLOv5 Documentation](https://docs.ultralytics.com/yolov5/).

Feel free to explore and adapt the project based on your preferences and specific game requirements.
