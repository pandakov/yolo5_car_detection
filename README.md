## YOLOv5 and EasyOCR based car liecense plate detection.

This code can detect russian liecense car plates.
### Detection
- run pip install -r requirements.txt to install dependencies
- put your weights on /weigths/best.pt (on Mac you can use /weigts/best.mlmodel for fast CoreML implementation)
- run carplate_detect.py to start recognizing test video
- for using detection script with video stream change 'source' parameter on detection_settings.json

### Training model
We build trainnig process for running on Google Colab https://colab.research.google.com/. Use GPU acceleration for fast training.

- prepare your dataset on Roboflow site https://universe.roboflow.com/
- copy train.ipynb to Google Colab
- insert your Roboflow API key to third ceil
- run it with your training parameters
- copy weights from /content/yolov5/runs/train/yolov5s_results/weights/best.pt to /weigths/best.pt of this repository
- if you want run detection on Mac with Apple Silicone chips you should run 'python export.py --/weights/best.pt --include coreml'