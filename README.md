# multimodal-chinese-speech-analysis
An end-to-end computational pipeline for multimodal analysis of spontaneous Chinese speech, integrating automatic speech recognition, prosodic analysis, co-speech gesture processing, temporal alignment, and exploratory speech–gesture coordination analysis.

This repository contains computational work developed as part of my Master's research in Computational Linguistics at Saint Petersburg State University.

The project investigates spontaneous spoken Chinese from a multimodal perspective, combining linguistic content, prosodic signals, and co-speech gestures to study how communicative information is distributed across modalities and coordinated over time.

The repository is an ongoing research project. The current implementation provides a working proof-of-concept pipeline, while subsequent stages will extend the analysis to manually annotated multimodal data and learned representations.

## Research Focus

### Current Focus

The current research focuses on:

* spontaneous Chinese speech
* speech and language processing
* prosodic analysis
* co-speech gesture analysis
* speech–gesture temporal coordination
* multimodal speech representation

### Longer-Term Directions

The broader research agenda includes:

* linguistically motivated gesture annotation and classification
* multimodal representation learning
* pragmatic and discourse analysis
* integration of linguistic structure with acoustic and visual signals

The central research goal is to move beyond treating speech as a purely textual or acoustic signal and investigate how linguistic, prosodic, and visual information jointly contribute to meaning in spontaneous communication.


## Research Pipeline

The current computational pipeline follows this workflow:

```mermaid
flowchart TD
    video[Video]

    video --> audio[Audio]
    video --> visual[Visual]

    audio --> asr[Speech Recognition]
    asr --> speech_segments[Speech Segmentation]
    speech_segments --> prosody[Prosodic Features]

    visual --> gesture_analysis[Hand / Gesture Analysis]
    gesture_analysis --> gesture_events[Gesture Event Detection]
    gesture_events --> gesture_features[Gesture Features]

    prosody --> alignment[Temporal Alignment]
    gesture_features --> alignment

    alignment --> multimodal[Aligned Multimodal Features]
    multimodal --> coordination[Temporal Coordination Analysis]
    coordination --> pragmatic[Pragmatic / Discourse Analysis]
```

The pipeline integrates speech, prosodic, and visual information on a shared temporal axis, providing a computational basis for multimodal analysis of spontaneous communication.

## Current Demonstration

<img width="1389" height="490" alt="image" src="https://github.com/user-attachments/assets/641188e8-f173-43f7-a0af-02e1817ae4e3" />
<img width="1189" height="490" alt="image" src="https://github.com/user-attachments/assets/fdf09c62-adc1-4f45-a5b2-d4e97686b902" />
<img width="989" height="490" alt="image" src="https://github.com/user-attachments/assets/47de86b3-6259-4f4d-b284-719ae5c33c0d" />
<img width="1389" height="590" alt="image" src="https://github.com/user-attachments/assets/701c9c2d-d61f-414c-b2fd-51ed953195cd" />



## Computational Components

### 1. Speech Processing

The speech component currently includes:

* Chinese automatic speech recognition
* speech segmentation
* transcript processing
* temporal alignment of speech segments

The current prototype uses Whisper-based automatic transcription.

### 2. Prosodic Analysis

The current prototype extracts acoustic features including:

* fundamental frequency (F0)
* intensity
* segment-level variability of prosodic measures

Prosodic features are extracted over short temporal windows and aggregated for aligned speech segments.

### 3. Gesture Analysis

The visual component focuses on co-speech hand movement.

Current computational experiments include:

* hand landmark detection
* wrist movement tracking
* movement-based gesture event detection
* temporal alignment between gesture movement and speech

The current gesture component is a prototype based on movement features. Linguistically motivated gesture categories, manual annotation, and supervised gesture classification are planned for later stages.

### 4. Multimodal Alignment

A central component of the project is the temporal integration of speech, prosodic, and visual information.

The current prototype aligns:

* speech transcripts
* speech timestamps
* F0 features
* intensity features
* wrist movement features
* speech–gesture temporal relationships

This provides a basis for exploratory analysis of how multimodal signals coordinate over time.

## Research Data

The research focuses on spontaneous spoken Chinese and audiovisual data suitable for multimodal analysis.

The current public demonstration uses one spontaneous Chinese speech video to validate the end-to-end processing pipeline.

Raw participant audio and video are not included in the public repository because the underlying recordings may contain personally identifiable information and human-subject data.

Publicly shareable materials are limited to code, documentation, derived non-sensitive examples, and other appropriate demonstration materials.

## Tools and Technologies

### Current Prototype

#### Programming and Data Analysis

* Python
* NumPy
* Pandas
* SciPy
* Scikit-learn

#### Speech and Audio Processing

* Whisper
* Praat
* Librosa

#### Visual Processing

* MediaPipe
* OpenCV

#### Deep Learning

* PyTorch

### Research Extensions

The broader research workflow may additionally involve:

* Hugging Face Transformers
* Universal Dependencies
* Stanza
* UDPipe
* ELAN
* CLIP
* Vision Transformers

These tools support subsequent work on linguistic structure, annotation, multimodal representation learning, and probing.

## Repository Structure

```text
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
```

## Current Status

The project is currently under development.

The current end-to-end prototype provides a working pipeline for:

```text
Video
  ↓
Chinese ASR
  ↓
Prosodic feature extraction
  ↓
Wrist movement extraction
  ↓
Temporal alignment
  ↓
Multimodal feature dataset
  ↓
Exploratory temporal coordination analysis
```

The current proof-of-concept has been tested on one spontaneous Chinese speech video and demonstrates:

* 1,846 video frames at 30 FPS
* 124 prosodic temporal windows
* 10 ASR segments
* 17 aligned multimodal features
* exploratory F0–gesture lag analysis
* event-based temporal matching

The current implementation is intended to validate the computational pipeline before scaling the analysis to a larger multimodal dataset.

## Planned Research Directions

Future development will focus on:

* developing a linguistically motivated annotation scheme for co-speech gestures
* building a manually annotated multimodal dataset
* improving gesture event segmentation and classification
* investigating speech–gesture temporal coordination at multiple timescales
* integrating linguistic structure with acoustic and visual signals
* studying pragmatic and discourse functions in spontaneous speech
* exploring multimodal representation learning and probing methods

## Research Motivation

Spontaneous communication is inherently multimodal. Speakers coordinate lexical, syntactic, prosodic, and visual signals rather than producing language through speech alone.

This project therefore treats speech, prosody, and gesture as complementary sources of communicative information and investigates how these signals can be represented and analyzed computationally.

The broader research goal is to develop computational approaches for understanding multimodal meaning and pragmatic information in natural communication.

## About

Xuanyu Zhang
M.S. Computational Linguistics
Saint Petersburg State University

Research interests:

Computational Linguistics · Multimodal NLP · Speech Processing · Gesture Analysis · Pragmatics · Multimodal Representation Learning

## Note

This repository represents ongoing academic research. Some components are experimental prototypes and may change as the research methodology, annotation framework, and modeling strategy develop.
