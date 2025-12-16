# Contents

## Project : Voice Based Speaker Recognition Using MFCC and LSTM

Project: Speaker Identification System

Course: ECE 5831 – Pattern Recognition and Neural Networks

University: University of Michigan – Dearborn

Team: Abbas Ali | Shravya Kumbham | Hesham Aldahbali

Date: 15 December 2025

## Overview
This project implements a voice-based speaker recognition system that identifies who is speaking from short speech recordings.
The system uses Mel-Frequency Cepstral Coefficients (MFCCs) for feature extraction and a Long Short-Term Memory (LSTM) neural
network to model temporal speech patterns.

Although the model achieved very high validation accuracy, real-world testing revealed a critical issue: the model was
learning recording device characteristics instead of speaker voice features. This project evolved into a controlled
experimental study that identified, proved, and fixed this issue.

## Dataset Used
1) Kaggle Dataset
   - Public speaker audio clips

2) YouTube Dataset
   - Speech extracted from public interviews

3) Custom Dataset
   - Speech recorded by team members

Dataset Split:
- Training:   70%
- Validation: 15%
- Testing:    15%

All audio was segmented into 1-second clips.

## Phases 

Phase 1 & 2: Public Datasets (Kaggle + YouTube)
- High validation accuracy
- Confirmed correctness of MFCC + LSTM pipeline

Phase 3: Custom Dataset (Failure Case)
- Validation accuracy > 95%
- Real-world testing failed completely
- Model misclassified speakers with high confidence

Discovery:
- Model was learning microphone/device signatures
- Device type was perfectly correlated with speaker label

Phase 4: Controlled Data Collection (Solution)
- All speakers recorded using the SAME device
- Device signature became constant across classes
- Model forced to learn voice characteristics

## Results
- Validation Accuracy: 95–98%
- Cross-Device Test Accuracy: ~96%
- Reliable speaker recognition on unseen recordings
- Demonstrated elimination of device bias

## Google drive Files Links

  - **Presentation Video:** https://drive.google.com/file/d/15CabA2xIFKZ77U94FIg-NlKPda9y-Av-/view?usp=drive_link
  - **Presentation Slides:** https://docs.google.com/presentation/d/1xJ5Yd5o2YuYNWNw6htODZbBF6Tqzk6bB/edit?usp=drive_link&ouid=112844933842032491009&rtpof=true&sd=true
  - **Project Report:** https://drive.google.com/file/d/1Dl946liJdNU5NPV_kZ22G3rNsRtTr7eb/view?usp=drive_link
  - **Dataset:** https://drive.google.com/file/d/16A31L332GTJN4WRg9sA39h7qNc6Lgrft/view?usp=drive_link
  - **Demo Video:** https://www.youtube.com/watch?v=V8Q1np9B8iw

## Note
While extracting the dataset zip folder please dont add any specific name to folder, just extract in the downloaded path.

Make sure to keep the ipynb file and dataset in same path for the code to work
