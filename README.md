# YOLOv8-CS2-Player-Recognition
This repository contains the implementation of YOLO v8 for detecting and recognizing players in the game CS2. It includes a detailed Jupyter Notebook with the complete pipeline from data preprocessing and model training to validation and real-world application, alongside the augmented dataset created using RoboFlow.

![Screenshot 2024-06-11 213505](https://github.com/mafazsyed/YOLOv8-CS2-Player-Recognition/assets/120568449/9bf8624d-5573-4d54-89fd-ed3808c4b430)

Data Collection: Gameplay videos were recorded and converted into images using FFmpeg to maintain high image quality, capturing one frame per second, avoiding repetitions in dataset.

Data Preparation: From these frames, 218 images containing visible players were selected and resized to 640 x 640.

Data Labeling: Each selected frame was manually annotated with bounding boxes around the players using RoboFlow, which facilitated precise and efficient labeling.

Data Augmentation: To enhance the model’s robustness and to generalize better, the following augmentation techniques were applied:

Horizontal flipping to allow the model to recognize players regardless of their orientation. Zooming (up to 25%) to train the model to detect players at various scales. Brightness adjustment (ranging from -15% to +15%) to simulate different lighting conditions that might occur in gameplay. This process generated 3 augmented images per original, totaling 654 training images.

Training Set Distribution: The dataset was split into 88% training (573 images), 8% validation (54 images), and 4% test sets (27 images).

![Screenshot 2024-06-11 213535](https://github.com/mafazsyed/YOLOv8-CS2-Player-Recognition/assets/120568449/4cbfd3f1-33c3-44a9-b761-cff79d21d9c4)
