How to setup and run the code
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

Dependencies
- `ultralytics==8.1.20` — YOLOv5 detection model
- `deep_sort_realtime==1.3.2` — DeepSORT tracker
- `opencv-python` — For video processing
- `torch` and `torchvision` — Required by YOLO and DeepSORT
- `numpy` — Numerical operations
