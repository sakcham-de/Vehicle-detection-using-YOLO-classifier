# Vehicle-detection-using-YOLO-classifier


This Python script uses the YOLO (You Only Look Once) real-time object detection system to detect vehicles in a video.

# YOLO classifier
The YOLO classifier used in this file is yolo version 8 classifiers for vehicles used from https://github.com/ultralytics/ultralytics 

## Dependencies

The script uses the following libraries:
- argparse: For command-line argument parsing.
- cv2: For reading and writing video files.
- numpy: For numerical operations.
- torch: For loading the YOLO model weights and performing the object detection.

## How it works

The script takes the following command-line arguments:
- `--source_weights_path`: The path to the YOLO model weights file.
- `--source_video_path`: The path to the source video file.
- `--target_video_path`: The path to the output video file.
- `--confidence_threshold`: The confidence threshold for the object detection.
- `--iou_threshold`: The Intersection Over Union (IOU) threshold for non-maximum suppression.

The `process_video` function is the main function that performs the vehicle detection. It reads the source video file, applies the YOLO object detection to each frame, and writes the frames with the detected vehicles to the target video file.

## Usage

Here's an example of how to run the script:

```shell
python vehicle_detection_yolo.py --source_weights_path /path/to/yolov8m.pt --source_video_path /path/to/video.mp4 --target_video_path /path/to/output.mp4
