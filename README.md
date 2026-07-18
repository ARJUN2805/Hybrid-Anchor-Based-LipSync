![Python](https://img.shields.io/badge/Python-3.10-blue)
![Librosa](https://img.shields.io/badge/Librosa-Audio%20Processing-green)
![FFmpeg](https://img.shields.io/badge/FFmpeg-Video%20Processing-orange)
![Whisper](https://img.shields.io/badge/OpenAI-Whisper-red)

# Hybrid-Anchor-Based-LipSync
Audio-driven video retiming for multilingual lip synchronization using hybrid temporal anchors.

## 📖 Overview

This project presents an **Audio-Driven Video Retiming Pipeline** for multilingual lip synchronization of dubbed educational videos.

Traditional lip synchronization techniques assume that the original and translated videos have identical durations, making frame-to-frame comparison unreliable when translation changes the speaking duration.

To overcome this limitation, this project introduces a **Hybrid Anchor-Based Temporal Alignment** approach that aligns the original video with translated speech using **long silence detection** and **temporal anchor mapping**, followed by segment-wise video retiming.

This work was developed as part of my **M.Tech Thesis in Artificial Intelligence & Data Science** at **Shiv Nadar University Chennai**.

# 🚀 Features

- Long Silence Detection
- Audio Energy Analysis
- Syllable Boundary Detection
- Boundary Correction
- Hybrid Anchor Mapping
- Segment-wise Video Retiming
- Motion Smoothing
- Whisper Word Timestamp Integration
- CPU Efficient Processing
- Automatic Timeline Alignment

# 🏗️ Project Workflow

Original Video
        │
        ▼
Extract Original Audio
        │
        ▼
Long Silence Detection
        │
        ▼
Silence Anchors
        │
        ▼
Translated Audio
        │
        ▼
Syllable / Word Boundary Detection
        │
        ▼
Boundary Correction
        │
        ▼
Hybrid Anchor Mapping
        │
        ▼
Timeline Alignment
        │
        ▼
Video Retiming
        │
        ▼
Motion Smoothing
        │
        ▼
Final Lip-Synced Video

# 🧠 Methodology

The proposed methodology consists of five major stages.

 ## 1. Long Silence Detection

- Load original audio
- Compute RMS Energy
- Adaptive Thresholding
- Detect Long Silence Regions
- Export Silence Anchors

## 2. Long Silence Correction

- Remove invalid silence intervals
- Preserve only meaningful silence anchors
- Generate corrected silence boundaries

## 3. Syllable Boundary Detection

- Segment translated speech
- Detect syllable boundaries
- Generate speech intervals
- Export boundary information

## 4. Boundary Correction

- Refine detected speech intervals
- Generate corrected boundary timestamps
- Prepare alignment anchors

## 5. Hybrid Anchor Mapping & Video Retiming

- Map silence anchors to translated timeline
- Align anchor points
- Perform segment-wise video retiming
- Apply motion smoothing
- Merge translated audio
- Generate synchronized output video

# 📊 Technologies Used

- Python
- Librosa
- NumPy
- Pandas
- Matplotlib
- OpenAI Whisper
- FFmpeg
- Google Colab

# 📈 Results

The proposed pipeline successfully

- Aligns original and translated timelines
- Preserves natural speech rhythm
- Reduces temporal mismatch
- Produces smooth video retiming
- Eliminates dependency on frame-by-frame comparison
- Runs efficiently on CPU without requiring GPU-based video generation models.

# 📷 Sample Outputs

### Long Silence Detection
<img width="1486" height="735" alt="long_silence_detection png" src="https://github.com/user-attachments/assets/52c4ba81-d08b-457c-9084-61c6a29667dd" />



### Syllable Boundary Detection

<img width="1477" height="557" alt="syllable_boundary_detection png" src="https://github.com/user-attachments/assets/24f2a59b-d433-498c-b222-2a6e41e3f2f0" />



### Timeline Alignment


<img width="1492" height="737" alt="alignment_plot png" src="https://github.com/user-attachments/assets/62d7d438-9b58-4984-9ff8-7caeb597aada" />


# ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Hybrid-Anchor-Based-LipSync.git
```
Install dependencies

```bash
pip install -r requirements.txt
```

# ▶️ Running the Project

Run the notebooks in the following order

1. Long Silence Detection
2. Long Silence Correction
3. Syllable Boundary Detection
4. Boundary Correction
5. Hybrid Anchor Mapping Pipeline

# 📚 Research Motivation

Multilingual dubbing introduces temporal differences because translated speech often differs in duration from the original speech.

Existing synchronization approaches rely on frame-to-frame comparison, which becomes unreliable when audio durations change.

This project proposes an audio-driven synchronization framework that uses temporal anchors extracted from speech to achieve efficient and scalable video synchronization.

# 🔮 Future Work

- RIFE Frame Interpolation
- FILM Frame Interpolation
- Phoneme-level Alignment
- Real-time Processing
- GPU Acceleration
- Automatic Video Dubbing Pipeline

# 👨‍💻 Author

**Arjun M P**

M.Tech Artificial Intelligence & Data Science

Shiv Nadar University Chennai

GitHub: https://github.com/ARJUN2805

LinkedIn:https://www.linkedin.com/in/arjun-m-p-214252217/

