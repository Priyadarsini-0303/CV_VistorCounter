## Visitor Face Recognition & Tracking System

This project implements a comprehensive face recognition and tracking system for detecting, identifying, and logging unique visitors in video streams or recorded video files. It leverages YOLOv8 for face detection, DeepSORT for multi-object tracking, and InsightFace for facial recognition embeddings. The solution stores visitor data and event logs in MongoDB Atlas and produces annotated output videos.

---

## Features

- Real-time face detection and tracking in videos or live streams.
- Accurate identification of unique faces with embedding matching.
- Persistent visitor and event storage via MongoDB Atlas.
- Visual output with rectangles and IDs on recognized faces.
- Support for video file and RTSP live stream inputs.

---

## Setup Instructions

1. Clone the repository.
2. Install required packages
3. Setup MongoDB Atlas and update your `config.json` with the connection string.
4. Run the main script with a video file or RTSP URL

## CONFIG FILE:
{
"mongodb_connection_string": "mongodb+srv://CV_TASK:12345@cluster-1.1aklqjp.mongodb.net/?retryWrites=true&w=majority&appName=Cluster-1",
"detection_model": "yolov8n.pt",
"tracker_max_age": 30,
"embedding_similarity_threshold": 0.6,
"log_directory": "logs/",
"output_directory": "output/"
}

---

## Architecture Diagram

<img width="1024" height="1024" alt="Arc_Image" src="https://github.com/user-attachments/assets/0d8fb672-aa13-4679-814e-0456c1962647" />


---

## Video Demonstration

Watch the explanatory and demonstration video here:

[![Watch the video](https://img.youtube.com/vi/VIDEO_ID/0.jpg)](https://www.loom.com/share/75dbe29d10e14d9f8fbf070552f6e9d3?sid=7efe7007-0059-4e2a-a299-1d76490e5899)


---

## Advancement Note

The current system uses YOLO for face detection, but we can enhance accuracy by replacing YOLO with the **RetinaFace model**, which provides superior face detection capabilities especially under challenging conditions.This implementation as been provided in the Advancement_CV_TASK.ipynb file in this gitub.
OUTPUT: ( bounds only the face properly )

<img width="1600" height="704" alt="image" src="https://github.com/user-attachments/assets/214dc206-1931-4fb2-ac7c-aa032a0e4b91" />

---

This project is a part of a hackathon run by [https://katomaran.com](https://katomaran.com).
