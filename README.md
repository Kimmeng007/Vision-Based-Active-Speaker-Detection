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

```mermaid
flowchart LR
    A[Input Video] --> B[YOLOv8 Face Detection]
    B --> C[Feature Extraction (ResNet50 / EfficientNetB0)]
    C --> D[LSTM for Temporal Modeling]
    D --> E[Speaker/Non-Speaker Classification]
    E --> F[Output: Active Speaker Detected]
```

## Dataset
The project uses a subset of data from the AVA-ActiveSpeaker Dataset, which provides synchronized video frames and speaker annotations.
Link to the dataset: https://research.google.com/ava/download.html#ava_active_speaker_download

## Key Features
- Real-time face detection using YOLOv8
- Temporal modeling via LSTM
- Camera control using OpenCV
- Visual experiment tracking using Weights & Biases (W&B)
- Modular and extendable PyTorch implementation

Check the full report of this project in the report folder.



