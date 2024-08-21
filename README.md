# Motion Detection and Alert System

## Overview

This project implements a real-time motion detection and alert system using Python, OpenCV, and Pygame. The system detects moving objects in a video stream (from a webcam or video file) and triggers an alert when motion is detected. The project includes two main scripts:

1. `region_of_interest.py`: Defines a specific region of interest (ROI) within the video frame and only triggers alerts when motion is detected within this area.
2. `sam3.py`: Detects motion across the entire video frame and plays an alert sound when significant movement is detected.

## Features

- **Motion Detection**: Uses background subtraction to detect moving objects in the video stream.
- **Region of Interest**: Allows specifying a polygonal ROI to focus motion detection on a specific area.
- **Alert System**: Triggers an audio alert when motion is detected.
- **Real-time Processing**: Processes video frames in real-time, displaying bounding boxes around detected objects and alerting the user.

## Requirements

- Python 3.x
- OpenCV
- NumPy
- Pygame

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/motion-detection-alert.git
   cd motion-detection-alert
   ```

2. Install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

3. Download and place the alert sound (`beep-04.wav`) in the project directory.

## Usage

### Running the Motion Detection with ROI

To run the motion detection with a defined region of interest, execute the `region_of_interest.py` script:

```bash
python region_of_interest.py
```

This script focuses on detecting motion within a specific area of the frame and triggers an alert if motion is detected within the ROI.

### Running the Full-Frame Motion Detection

To run the motion detection across the entire frame, execute the `sam3.py` script:

```bash
python sam3.py
```

This script monitors the entire video frame for motion and plays an alert sound when motion is detected.

### Customizing the Region of Interest

The ROI is defined in the `region_of_interest.py` script as a polygon with coordinates:

```python
roi = [(100, 100), (500, 100), (500, 400), (100, 400)]
```

You can modify these coordinates to set a custom ROI based on your needs.

## Dependencies

- **OpenCV**: For video processing and motion detection.
- **NumPy**: For array manipulation and ROI handling.
- **Pygame**: For playing the alert sound when motion is detected.

## Contributing

Contributions are welcome! If you find a bug or want to add new features, feel free to submit a pull request.
