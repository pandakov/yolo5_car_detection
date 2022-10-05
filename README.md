## YOLOv5 and EasyOCR based car liecense plate detection.

This code can detect russian liecense car plates.
### Detection
- run pip install -r requirements.txt to install dependencies
- put your weights on /weigths/best.pt (on Mac you can use /weigts/best.mlmodel for fast CoreML implementation)
- run carplate_detect.py to start recognizing test video
- for using detection script with video stream change 'source' parameter on detection_settings.json

#### Training model
We build trainnig process for running on Google Collab https://colab.research.google.com/
For trainnig YOLOv5 model copy train.ipynb to collab and run it.