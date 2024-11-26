<div align="center">

# AI Video Caption and Generation System

[![Gradio](https://img.shields.io/badge/Gradio-FF6B6B?style=for-the-badge&logo=gradio&logoColor=white)](https://gradio.app/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](https://opencv.org/)
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org/)

This project integrates the powerful AnimateDiffPipeline and BLIP (Bootstrapped Language-Image Pre-training) models to create an advanced text-to-video generation system. The application allows users to generate visually compelling animations based on text prompts with optional motion effects. Built using Hugging Face Diffusers and Gradio, the project features customizable motion adapters, base models, and user-friendly deployment.

</div>

## 📑 Table of Contents
- [Features](#-features)
- [Demo](#)
- [Setup Instructions](#%EF%B8%8F-setup-instructions)
- [Installation](#-installation)
- [Usage](#-usage)
- [Technical Details](#-technical-details)
- [Project Structure](#-project-structure)
- [Dependencies](#-dependencies)
- [Model Details](#model-details)
- [Configuration](#%EF%B8%8F-configuration)
- [Troubleshooting](#%EF%B8%8F-troubleshooting)
- [Processing Pipeline](#-processing-pipeline)
- [License](#-license)

## ⚡ Features

**Transform descriptive text into captivating animations.**

**Base Models:**

* Realistic
* Cartoon
* Anime
* 3D

**Dynamic Motions:**

* Zoom In / Out
* Pan Left / Right
* Tilt Up / Down
* Roll Clockwise / Anticlockwise

**BLIP Integration:**

* Enhance visual storytelling with BLIP's pre-trained models for captioning and fine-tuning.

**Adjustable Inference Steps:**

* Control animation quality and speed through step adjustments.

**Interactive Gradio Interface:**

* Generate and download videos seamlessly via the web app.
## 🎞️ Demo
We’ve created a short demo video showcasing the functionality of our AI Video Caption and Generation System. From extracting frames and generating captions using BLIP to producing motion-enhanced AI-generated videos, the demo highlights each step of the pipeline.
[Watch the Demo](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

## ⚙️ Setup Instructions
1. Clone the Repository
   * Clone the repository from Hugging Face using Git Large File Storage (LFS):
```bash
git clone https://huggingface.co/spaces/orderlymirror/Text-to-Video
cd Text-to-Video
```
2. Install Dependencies
   * Install the required libraries for the project:
```bash
pip install -r requirements.txt
```
3. Run the Application
   * Launch the Gradio interface:
```bash
python app.py
```
   * The application will be available at http://localhost:7860 or a shareable link.
   
## 🔧 Installation

```bash
# Clone the repository
git clone https://github.com/Hemanth1818/ai-video-caption-and-generation-system
cd ai-video-caption-and-generation-system

# Install required packages
pip install gradio
pip install transformers
pip install opencv-python-headless
pip install diffusers
pip install torch
```

## 🚀 Usage
- Enter a Prompt: Describe the animation you'd like to generate (e.g., "A futuristic city with flying cars").
- Select Style: Choose a base model for the animation (e.g., "Realistic," "Anime").
- Apply Motion: Add motion effects like zoom or tilt for dynamic output.
- Set Inference Steps: Choose the level of detail and quality by adjusting the inference steps.
- Submit: Click the generate button and watch your video come to life!
![image](https://github.com/user-attachments/assets/eb2ff358-d586-4f71-aced-e0faf40ecfab)

## 💻 Technical Details

### Video Processing Pipeline
```python
# Extract frames
frames = extract_frames(video_path, frame_rate=1)

# Generate captions using BLIP
captions = generate_captions_with_blip(frames)

# Create AI-generated video
generate_video_from_captions('captions.txt', 'output_video.mp4')
```

## 📁 Project Structure

```
.Text-to-Video
├── app.py                # Main Gradio interface code
├── requirements.txt      # Dependencies for the project
├── README.md             # Project documentation
├── style.css             # (Optional) Custom Gradio styles
└── assets/
    └── sample_video.mp4  # Sample output video

```

## 📦 Dependencies

- Python 3.8+
- gradio
- transformers==4.30.0+
- opencv-python-headless
- diffusers
- torch>=2.0.0
- Pillow
- numpy

## Model Details

| Model | Description |
|---|---|
| BLIP | Captioning and language-vision alignment |
| AnimateDiff | Text-to-video synthesis pipeline |
| Base Models | Pre-trained artistic generators |
| Motion Adapters | Adds dynamic animations like zoom and pan |

## 🛠️ Configuration

```python
# Frame extraction settings
FRAME_RATE = 1  # Frames per second
FRAME_SIZE = (1920, 1080)
FPS = 24

# Video output settings
VIDEO_FORMAT = 'mp4v'
```

## ⚠️ Troubleshooting

Common Issues:
```
1. CUDA Out of Memory
   Solution: Reduce batch size or frame rate

2. Video Loading Error
   Solution: Ensure video format is supported (mp4, avi)

3. Model Loading Issues
   Solution: Check internet connection and HuggingFace login
```

## 🔄 Processing Pipeline

1. Extract Frames → Process with BLIP for captioning.
2. Text Input (captions) → AnimateDiffPipeline.
3. Frames → Motion Adapter for animations.
4. Generated Frames → Export to Video.

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
