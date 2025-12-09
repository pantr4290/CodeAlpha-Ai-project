# Task 4 – Object Detection and Tracking (YOLO + Tracking)

## Steps Implemented

1. **Real-time Video Input**
   - Uses the default **webcam** (`source=0`) via Ultralytics + OpenCV backend.

2. **Pre-trained Object Detection Model**
   - Uses **YOLOv8 nano** model: `yolov8n.pt`.
   - Automatically downloaded by `ultralytics` if not present.

3. **Frame-wise Object Detection**
   - Each frame is processed to detect objects.
   - YOLO outputs bounding boxes, class labels, and confidence scores.

4. **Object Tracking**
   - Uses built-in tracking with **BoT-SORT** (via `botsort.yaml`).
   - Each detected object gets a **tracking ID** that persists across frames.

5. **Real-time Display**
   - Output window shows:
     - Bounding boxes
     - Class labels (e.g., person, car, dog)
     - Tracking IDs
   - Updates in real time as the webcam feed changes.

## How to Run

```bash
cd task4_object_detection_tracking
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # macOS / Linux

pip install -r requirements.txt
python detect_and_track.py
