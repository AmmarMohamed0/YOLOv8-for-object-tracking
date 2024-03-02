# YOLOv8-for-object-tracking
Loading YOLOv8 Model:
- This line initializes the YOLOv8 model for object detection and tracking.

Opening Video File:
- The script opens a video file specified by the `video_path` variable for processing.

Track History:
- Creates a dictionary named `track_history` to store the track history of detected objects.
- It utilizes `defaultdict` from the `collections` module, allowing a default value (an empty list) to be set for any new key.

Processing Video Frames:
- The script iterates through each frame of the video for object detection and tracking.

Object Detection and Tracking:
- Reads a frame from the video and applies YOLOv8 for object detection and tracking.
- The `persist=True` parameter ensures the tracking continues between frames.

Extracting Object Information:
- Extracts information about detected objects, such as their bounding boxes and IDs.

Visualizing Results:
- Generates an annotated frame with bounding boxes around detected objects.

Updating Track History:
- For each detected object, updates its track history by appending its current position to the corresponding list in `track_history`.

Drawing Tracks:
- Draws tracks for detected objects using their track history.
- Lines are drawn to connect previous positions of the objects.

Displaying Annotated Frame:
- Displays the annotated frame with detected objects and their tracks.

Exiting the Loop:
- The loop continues until the end of the video or until the user presses 'q' to exit.

Cleaning Up:
- Releases the video capture object and closes the display window after processing the video.
