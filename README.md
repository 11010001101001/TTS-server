# 🎙️ TTS Voice Synthesis Server

> Fast, lightweight neural text-to-speech streaming service powered by FastAPI and Coqui TTS.

---

## 🌟 Overview

A Python-based microservice that delivers real-time voice synthesis and zero-shot voice cloning over HTTP. Designed for low-latency streaming and expressive speech generation.

## ✨ Features

- **Real-Time Streaming**: Low-latency audio streaming (`audio/wav`) via FastAPI `StreamingResponse`.
- **Zero-Shot Voice Cloning**: Clones reference speaker characteristics from short audio samples.
- **Multi-Voice Support**: Built-in voice profiles for rapid switching.
- **RESTful API**: Clean `POST /tts` endpoint accepting custom synthesis payloads.

## 🛠️ Tech Stack

- **Framework**: FastAPI, Uvicorn
- **Speech Synthesis**: Coqui TTS, PyTorch
- **Audio Processing**: SoundDevice, PyAudio, NumPy

## 🚀 Quick Start

1. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Run the server:**
   ```bash
   python main.py
   ```
   The service will start on `http://0.0.0.0:8000`.

3. **Synthesize speech:**
   ```bash
   curl -X POST "http://localhost:8000/tts"         -H "Content-Type: application/json"         -d '{"text": "Hello, world!"}'         --output output.wav
   ```
