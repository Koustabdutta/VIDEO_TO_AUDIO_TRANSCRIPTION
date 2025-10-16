# 🎥 Whisper-Powered Video & Audio Transcription Service

An end-to-end project that fine-tunes the state-of-the-art **Whisper** model for Automatic Speech Recognition (ASR) and deploys it as a user-friendly web interface using **Gradio**. This service allows users to upload video or audio files and receive an accurate text transcript.

---

## ✨ Features

* **Advanced ASR:** Utilizes a **fine-tuned Whisper model** for highly accurate transcription.
* **Model Optimization:** Includes a training pipeline (`Video_to_text.ipynb`) using the **LibriSpeech ASR corpus** to minimize the Word Error Rate (WER).
* **Media Versatility:** Supports both **video** and **audio** file uploads for transcription.
* **Web Interface:** Deployed via an intuitive **Gradio** application, which launches a shareable public link.
* **Media Processing:** Uses **MoviePy** and **pydub** to automatically extract audio from video files before transcription.

---

## 🛠️ Technology Stack

| Component | Technology / Library | Purpose |
| :--- | :--- | :--- |
| **Model** | **Whisper** (Hugging Face Transformers) | Core ASR model. |
| **Framework** | **PyTorch**, **Accelerate** | Deep learning and optimized training. |
| **Interface** | **Gradio** | Web application UI for uploads and results. |
| **Media Handling** | **MoviePy**, **pydub** | Video processing and audio extraction. |
| **Data & Metrics** | `datasets`, `librosa`, `jiwer` | Data loading, audio processing, and evaluation (WER). |

---

## 🚀 Setup and Installation

### 1. Environment Setup

It's highly recommended to use a dedicated environment (e.g., Conda or venv). **For model fine-tuning, a CUDA-enabled GPU is necessary.**

### 2. Install Dependencies

Run the following commands to install all required libraries. The first command installs the necessary PyTorch version.

```bash
# Install PyTorch with CUDA support (adjust index-url for your system)
pip install torch torchvision torchaudio --index-url [https://download.pytorch.org/whl/cu121](https://download.pytorch.org/whl/cu121)

# Install core ASR, training, and application packages
pip install transformers datasets librosa soundfile jiwer evaluate accelerate
pip install gradio moviepy pydub
