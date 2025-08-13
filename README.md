# TTS + Lip-Sync Video Generation using Wav2Lip

## Overview
  This project generates a 30–45 second speaking video by:
    Converting text to speech (TTS) using Google Text-to-Speech (gTTS).
    Lip-syncing the generated audio to a still face video using Wav2Lip.

## 📁 Repository Contents
wav2lip-tts-assignment.ipynb → Main notebook containing the full implementation code
still_video.mp4 → input video(data)
output_video_tts.mp4 → Final generated lip-synced output video

## 📂 Project Structure
  Alethea_AI/
      still_video.mp4          # Still face video (used as dataset)
      input_audio_tts.wav      # Generated TTS audio
      output_video_tts.mp4     # Final lip-synced video
  Wav2Lip/                     # Cloned Wav2Lip repo

## 🛠 Installation & Setup
  ### 1. Environment
    Python version: 3.10+
    Hardware requirement: GPU (T4 or better recommended)
    Tested on: Kaggle Notebook with NVIDIA T4 GPU
  
  ### 2. Clone Wav2Lip
    git clone https://github.com/Rudrabha/Wav2Lip.git
    cd Wav2Lip
    pip install -r requirements.txt
    pip install gdown
  
  ### 3. Fix compatibility issues
    pip install numpy==1.23.5 librosa==0.9.2
    pip install gtts

  ### 4. Download pretrained model
    mkdir -p checkpoints
    cd checkpoints
    wget -O wav2lip_gan.pth "https://huggingface.co/Nekochu/Wav2Lip/resolve/main/wav2lip_gan.pth"
    cd ..

## 🚀 How to Run
    Prepare the environment (Kaggle or local machine with GPU)
    Clone Wav2Lip and install dependencies
    Download pretrained model
    Prepare input video and generate TTS audio
    Run inference to produce lip-synced output
    View final MP4 video

## Output
    You can find the final generated video in:
    /kaggle/working/Alethea_AI/output_video_tts.mp4
    
## 📌 Known Limitations
    Works best with frontal face and clear audio.
    Requires GPU for real-time or faster processing.
    No multi-segment stitching or streaming implemented.

## 📜 Attribution
    Wav2Lip Repository by Rudrabha et al.
    Pretrained model from Hugging Face
    TTS powered by Google Text-to-Speech (gTTS)

