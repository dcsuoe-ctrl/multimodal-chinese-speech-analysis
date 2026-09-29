# multimodal-chinese-speech-analysis
Computational pipeline for multimodal analysis of spontaneous Chinese speech, integrating speech, prosody, co-speech gestures, and temporal alignment.
This repository contains the computational work developed as part of my Master's research in Computational Linguistics at Saint Petersburg State University.

The project investigates spontaneous spoken Chinese from a multimodal perspective, integrating speech content, prosody, and co-speech gestures to study how different communicative signals interact over time and contribute to linguistic, pragmatic, and discourse-level interpretation.

The repository is a work in progress and will be continuously updated as the research develops.

Research Focus:

The project currently focuses on:

Spontaneous Chinese speech
Speech and language processing
Prosodic analysis
Co-speech gesture analysis
Temporal coordination between speech and gesture
Multimodal representation learning
Pragmatic and discourse functions

The central research idea is to move beyond speech as a purely textual or acoustic signal and investigate how linguistic, prosodic, and visual information jointly contribute to meaning in spontaneous communication.

Research Pipeline:

The current computational pipeline follows this general workflow:

                    Video
                      │
          ┌───────────┴───────────┐
          │                       │
        Audio                   Visual
          │                       │
          ▼                       ▼
   Speech Recognition       Hand / Gesture Analysis
          │                       │
          ▼                       ▼
   Speech Segmentation      Gesture Segmentation
          │                       │
          ▼                       ▼
   Prosodic Features        Gesture Features
          │                       │
          └───────────┬───────────┘
                      ▼
             Temporal Alignment
                      │
                      ▼
          Multimodal Representation
                      │
                      ▼
       Pragmatic / Discourse Analysis

Computational Components
1. Speech Processing

The speech component includes:

Chinese automatic speech recognition
speech segmentation
transcript processing
temporal alignment of speech segments

Current experiments use Whisper-based automatic transcription.

2. Prosodic Analysis

The project extracts acoustic features including:

fundamental frequency (F0)
intensity
duration
variability of prosodic measures

These features are analyzed at the level of speech segments and in relation to visual signals.

3. Gesture Analysis

The visual component focuses on co-speech hand gestures.

Current computational experiments include:

hand landmark detection
hand movement tracking
gesture event segmentation
preliminary gesture identification and classification
temporal alignment between gestures and speech

The current gesture classification is a prototype. Linguistically motivated gesture categories and manually annotated data will be used for subsequent research stages.

4. Multimodal Alignment

A central part of the project is the temporal integration of different modalities.

For each speech segment, the system can combine:

transcript
speech duration
prosodic features
gesture occurrence
gesture duration
gesture type
speech–gesture temporal overlap

This provides a basis for studying how multimodal signals coordinate during spontaneous communication.

Research Data:

The research is based on spontaneous spoken Chinese data, including audiovisual recordings suitable for multimodal analysis.

Because the data may contain personally identifiable information and human-subject recordings, raw participant video and audio are not included in this public repository.

Only code, documentation, synthetic examples, and/or appropriately shareable demonstration materials are intended for public release.

Tools and Technologies:

The project currently uses:

Programming & Data Analysis

Python
NumPy
Pandas
Scikit-learn

Speech & Language Processing

Whisper
Hugging Face Transformers
Universal Dependencies
Stanza / UDPipe

Audio & Prosody

Praat
Librosa

Visual / Multimodal Processing

MediaPipe
OpenCV
Vision Transformers
CLIP

Annotation

ELAN

Deep Learning

PyTorch
Repository Structure
multimodal-chinese-speech-analysis/
│
├── src/
│   ├── asr.py
│   ├── prosody.py
│   ├── gesture.py
│   ├── align.py
│   └── pipeline.py
│
├── notebooks/
│   └── 01_end_to_end_demo.ipynb
│
├── docs/
│   └── annotation_scheme.md
│
├── data/
│   └── README.md
│
├── outputs/
│   └── README.md
│
├── requirements.txt
├── run_pipeline.py
└── README.md
Current Status

The project is currently under development.

The existing implementation provides a working prototype for:

Video
→ Chinese ASR
→ Prosodic feature extraction
→ Hand tracking
→ Preliminary gesture analysis
→ Speech–gesture temporal alignment

The research is gradually moving from rule-based and exploratory processing toward manually annotated multimodal data, supervised classification, and multimodal representation learning.

Planned Research Directions

Future development will focus on:

improving the annotation scheme for co-speech gestures;
building a manually annotated multimodal dataset;
training supervised gesture classification models;
investigating speech–gesture temporal coordination;
integrating linguistic structure with acoustic and visual signals;
studying pragmatic and discourse functions in spontaneous speech;
exploring multimodal representation learning and probing methods.
Research Motivation

Spontaneous communication is inherently multimodal. Speakers coordinate lexical, syntactic, prosodic, and visual signals rather than producing language through speech alone.

This project therefore treats speech, prosody, and gesture as complementary sources of communicative information and investigates how they can be represented and analyzed computationally.

The broader goal is to develop computational approaches for understanding multimodal meaning and pragmatic information in natural communication.

About

Xuanyu Zhang
M.S. Computational Linguistics
Saint Petersburg State University

Research interests:

Computational Linguistics · Multimodal NLP · Speech Processing · Gesture Analysis · Pragmatics · Multimodal Representation Learning

Note

This repository represents ongoing academic research. Some components are experimental prototypes and may change as the research methodology and annotation framework develop.
