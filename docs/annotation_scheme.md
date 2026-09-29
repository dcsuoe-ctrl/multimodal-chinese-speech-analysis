# Multimodal Annotation Scheme

## 1. Overview

This document describes the working annotation framework for multimodal analysis of spontaneous Chinese speech.

The scheme is designed to support the study of speech, prosody, and co-speech gesture, with particular attention to their temporal coordination and potential pragmatic and discourse functions.

The annotation framework is currently under development and will be refined through pilot annotation.

## 2. Annotation Units

The main annotation units are:

* speech segments
* prosodic windows
* gesture units

### Speech Segment

A temporally bounded unit of spoken content containing:

* start time
* end time
* transcript

### Prosodic Window

The current computational prototype uses 0.5-second windows for:

* fundamental frequency (F0)
* intensity

### Gesture Unit

A visually identifiable hand movement that accompanies or contributes to spontaneous communication.

Each gesture unit may include:

* start time
* end time
* hand
* gesture type
* speech–gesture temporal relation
* optional pragmatic or discourse function

## 3. Gesture Types

The initial working taxonomy includes:

### Deictic

Gestures used to indicate a person, object, location, direction, or discourse referent.

### Iconic

Gestures that depict an object, action, spatial configuration, or event.

### Beat

Rhythmic hand movements accompanying speech without directly depicting a concrete referent.

### Emblematic

Conventionalized gestures with a relatively stable communicative meaning.

### Other

Gestures that do not fit the categories above.

### Uncertain

Used when the available audiovisual evidence is insufficient for reliable classification.

These categories are provisional and may be revised during pilot annotation.

## 4. Speech–Gesture Temporal Relation

The annotation framework distinguishes
