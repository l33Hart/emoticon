# emoticon

Emoticon is a full-stack AI-powered application designed to detect and visualize human emotions using both facial expressions and speech patterns. This project combines convolutional neural networks (CNNs) trained on grayscale images and audio spectrograms with a user-friendly ASP.NET Razor Pages frontend.

---

## Project Goals

- Emotion Detection from facial and vocal cues
- Real-time Visualization for user and admin dashboards
- Multi-Modal AI using two independent models: vision and sound
- Clean UI built with ASP.NET Razor Pages (no JavaScript frameworks)
- Local-first development using Docker and Git Student Host

---

## AI Models

### 1. Facial Expression Model (Visual CNN)
- Input: 64x64 grayscale images
- Architecture:
  - Deep CNN with 3 convolutional blocks
  - Heavy batch normalization
  - L2 regularization
  - Exponential learning rate decay
- Accuracy: ~94 percent (Training), ~69 percent (Validation)
- Data Augmentation: Enabled

### 2. Voice Emotion Model (Audio CNN)
- Input: Spectrograms generated from audio (.wav) files
- Architecture:
  - Spectrogram-based CNN with layer normalization
  - No augmentation to preserve emotional fidelity
- Public Datasets: RAVDESS, CREMA-D, EmoDB
- Output: Emotion class (e.g., Happy, Angry, Neutral)

---

## Tech Stack

| Layer       | Technology                   |
|-------------|------------------------------|
| Frontend    | ASP.NET Razor Pages          |
| Backend     | C# (.NET Core), Python       |
| AI Framework| TensorFlow, Keras            |
| Deployment  | Docker, Git Student Host     |
| Database    | SQL Server or Lite DB (TBD)  |

---

## Development Timeline

| Phase           | Time Frame    |
|-----------------|---------------|
| Model Training  | Sprint 1 to 2 |
| UI Development  | Sprint 3 to 4 |
| Integration     | Sprint 5      |
| Deployment      | Final Week    |

---

## Features

- Login for users and staff
- Upload images or audio for real-time prediction
- Emotion dashboard with status indicators
- Model accuracy display and visual feedback
- Admin panel for dataset review and testing

---

## Folder Structure

emoticon/
|
├── facial_images_resized/      - Vision training data  
├── spectrograms/               - Audio training data  
├── models/                     - Saved model files  
├── EmoticonWebApp/             - ASP.NET Razor frontend  
├── main.py                     - Python AI model handler  
├── Dockerfile                  - Containerization setup  
└── README.md                   - Project overview

---

## Setup Instructions

