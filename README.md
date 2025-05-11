---

### 📘 README.md — Real-Time Audio Classification using YAMNet

#### 🧠 Project Overview

This project uses **YAMNet**, a pretrained audio classification model built on MobileNet and trained on **AudioSet**, to perform **real-time sound event detection**. It supports both microphone and audio file inputs and classifies sounds into over 500 audio classes.

---

#### 📁 Project Structure

1. **# Real-Time Classification**

   * Loads and runs `YAMNet` from TensorFlow Hub.
   * Uses `librosa` for audio preprocessing.
   * Classifies incoming audio clips and returns the top predicted label.
   * Optionally uses a separate classifier trained on embeddings extracted from YAMNet for custom tasks (e.g., ESC-50 or UrbanSound).

---

#### 🚀 Getting Started

1. **Install Dependencies**

   ```bash
   pip install tensorflow tensorflow_hub librosa gradio numpy
   ```

2. **Run the Notebook**

   * Upload your audio file (e.g., `.wav`, `.mp3`), or speak into the microphone (if enabled).
   * The model extracts embeddings and returns a predicted label.

---

#### 🛠️ How It Works

* **Audio Input**: Captures 10 seconds of audio.
* **Preprocessing**: Converts raw audio into the required input format.
* **Embedding Extraction**: Passes waveform to YAMNet to get high-level feature embeddings.
* **Classification**:

  * Option 1: Use YAMNet's built-in output classes.
  * Option 2: Train a custom classifier on the embeddings (e.g., for ESC-50 tasks).

---

#### 💡 Features

* Real-time prediction
* Audio waveform slicing
* Embedding averaging
* Interactive interface using **Gradio**

---

#### 📎 Notes

* YAMNet supports over 500 classes from the AudioSet ontology.
* Custom classifiers can be plugged in for specific tasks using the embeddings.

---
