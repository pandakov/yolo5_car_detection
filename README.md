## YOLOv5 and EasyOCR based car liecense plate detection.

This code can detect russian liecense car plates.
### Detection
- run pip install -r requirements.txt to install dependencies
- put your weights on /weigths/best.pt (on Mac you can use /weigts/best.mlmodel for fast CoreML implementation)
- run carplate_detect.py to start recognizing test video
- for using detection script with video stream change 'source' parameter on detection_settings.json

### Training model
We built trainnig process for running on Google Colab https://colab.research.google.com/. Use GPU acceleration for fast training.

- prepare your dataset on Roboflow site https://universe.roboflow.com/
- copy train.ipynb to Google Colab
- insert your Roboflow API key to third ceil
- run it with your training parameters
- copy weights from /content/yolov5/runs/train/yolov5s_results/weights/best.pt to /weigths/best.pt of this repository
- if you want run detection on Mac with Apple Silicone chips you should run 'python export.py --/weights/best.pt --include coreml'

### Metrics
Some metrics of training YOLOv5 model you can see below. There are dataset with 519 images downloaded from Roboflow.
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/25423296/163456776-7f95b81a-f1ed-45f7-b7ab-8fa810d529fa.png">
  <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>