How to setup and run the code:
1. Install the required dependencies:
  !pip install ultralytics
  !pip install deep_sort_realtime
  !pip install opencv-python
  !pip install ipywidgets
2. Project Files Overview:
  player_tracking.ipynb
  v3.mp4 (input video)
  v3_annotated (6).mp4 (output video)
3. Model is provided in google drive (https://drive.google.com/drive/folders/1HDFwT7dVYkuEbYLtHZlKhtxNm_jp9gAA?usp=sharing)
4. Run the notebook

Dependencies:
- `ultralytics==8.1.20` — YOLOv11 detection model
- `deep_sort_realtime==1.3.2` — DeepSORT tracker
- `opencv-python` — For video processing
- `torch` and `torchvision` — Required by YOLO and DeepSORT
- `numpy` — Numerical operations

Google Drive link(https://drive.google.com/drive/folders/1HDFwT7dVYkuEbYLtHZlKhtxNm_jp9gAA?usp=sharing) it includes model, input, output, report

Summary:
-Used YOLOv11-based model (best.pt) to detect ball, goalkeeper, player, and referee.
-Focused only on class 2 (player) for tracking.
-Ran detection frame-by-frame on sports video input.
-Shrunk YOLO bounding boxes by 40% to improve focus and reduce noise.
-Used DeepSORT for tracking players and assigning consistent IDs.
-Saved annotated output video with bounding boxes and player IDs.
-Bounding boxes were often too large or imprecise from the model.
-DeepSORT IDs frequently switched due to box drift or occlusions.
-Extra or duplicate detections occurred due to overlapping or misclassified boxes.
-Output video worked but was unstable in long occlusion scenes.
-Main issues: loose boxes, ID switching, and overlapping detections.
-Needs better YOLO training with tighter labels and consistent annotations.
-Appearance model in DeepSORT could be upgraded for better ID consistency.
-Project successfully demonstrates detection and basic tracking of players.


