# Vehicle Count and Detection

This project involves detecting and counting vehicles using computer vision techniques. It leverages OpenCV for real-time object detection and tracking. The system captures video input, detects vehicles, and tracks them across frames to maintain a consistent count.

## Project Files

1. **tracker.py**: Contains the `EuclideanDistTracker` class for tracking objects based on their Euclidean distance between frames.
2. **vehicle_count.py**: Main script that utilizes the tracker to count and display detected vehicles in a video feed.

## How It Works

### tracker.py
The `EuclideanDistTracker` class maintains a dictionary of object center points and assigns unique IDs to detected objects. The `update` method matches new detections with existing objects based on the Euclidean distance and updates their positions.

### vehicle_count.py
1. **Video Capture**: The script captures video from a file (`highway.mp4`).
2. **Region of Interest (ROI)**: Defines a region of interest in the frame for detection.
3. **Object Detection**: Uses `cv2.createBackgroundSubtractorMOG2` for background subtraction to detect moving objects.
4. **Contour Detection**: Finds contours in the mask to identify potential vehicles.
5. **Tracking**: Updates the tracker with detected bounding boxes and assigns unique IDs to each vehicle.
6. **Visualization**: Draws bounding boxes and IDs on the ROI and displays the frames.

## Real-Life Impact

This vehicle detection and counting system can be utilized in various real-life scenarios:

1. **Traffic Monitoring**: Helps in monitoring traffic flow and density on highways.
2. **Parking Management**: Assists in managing parking spaces by counting incoming and outgoing vehicles.
3. **Toll Collection**: Enhances automated toll collection systems by accurately counting vehicles.
4. **Smart Cities**: Contributes to smart city initiatives by providing data for traffic management and urban planning.

## Getting Started

### Prerequisites

- Python 3.x
- OpenCV (`pip install opencv-python`)

### Running the Project

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/vehicle-count-detection.git
    ```
2. Navigate to the project directory:
    ```sh
    cd vehicle-count-detection
    ```
3. Run the main script:
    ```sh
    python vehicle_count.py
    ```

