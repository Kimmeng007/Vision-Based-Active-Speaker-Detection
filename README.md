# Vision-Based-Active-Speaker-Detection
This project focuses on **active speaker detection (ASD)** using **only visual information** — identifying which person in a video is speaking without relying on audio cues. The system combines **deep convolutional neural networks (CNNs)** for spatial feature extraction with **LSTM** networks for temporal modeling, providing an efficient solution for robotic and real-time applications.

---

## Project Overview
Active Speaker Detection plays a crucial role in human–robot interaction, video conferencing, and surveillance systems.  While many existing approaches use both **audio and visual modalities**, this project aims to build a **visual-only system**, enabling reliable speaker detection even in noisy environments or when audio is unavailable.

The proposed model leverages:
- **YOLOv8** for real-time **face detection**
- **ResNet50** and **EfficientNetB0** as CNN backbones for feature extraction
- **LSTM** for temporal dynamics modeling across frames
- **SORT (Simple Online and Real-time Tracking)** for consistent identity tracking
- **OpenCV** for camera control and video processing

---

## System Architecture
The system pipeline is organized into several main stages:
1. **Input Video Processing** – A video stream is captured and preprocessed using OpenCV.  
2. **Face Detection** – YOLOv8 detects faces in each frame with bounding boxes.  
3. **Feature Extraction** – Each detected face is passed through a CNN backbone (ResNet50 or EfficientNetB0) to obtain spatial embeddings.  
4. **Temporal Modeling** – The sequence of embeddings over time is fed into an LSTM network to capture motion and temporal patterns.  
5. **Classification** – The LSTM output is classified as either **“Speaking”** or **“Not Speaking”**.  
6. **Output Visualization** – The result is overlaid on the video, and active speakers are highlighted in real time.

## Dataset
The project uses a subset of the AVA-ActiveSpeaker Dataset, which provides synchronized video frames and speaker annotations.
Link to the dataset: https://research.google.com/ava/download.html#ava_active_speaker_download

## Key Features
- Real-time face detection using YOLOv8
- Temporal modeling via LSTM
- Camera control using OpenCV
- Visual experiment tracking using Weights & Biases (W&B)
- Modular and extendable PyTorch implementation

Check the full report of this project in the report folder.



