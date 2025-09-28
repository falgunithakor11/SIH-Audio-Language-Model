# SIH-Audio-Language-Model
An Audio Language Model for joint speech &amp; non-speech understanding in Indian languages. A project for SIH 2025.
# The Indian Audio Scenes Dataset

This repository contains a high-quality, manually annotated dataset of complex audio scenes from various Indian contexts. It is designed to be used for training and evaluating Audio Language Models (ALMs) that require joint understanding of both speech and non-speech sounds.

---

## 1. Goal of the Dataset

The primary goal of this dataset is to provide rich, contextual audio data for training models on the "Listen, Think, and Understand" task. It is specifically created to address the lack of resources that combine:
* **Speech in Indian Languages:** Primarily Hinglish, capturing natural conversations.
* **Non-Speech Events:** A wide range of ambient and specific sounds found in real-world Indian environments.
* **Inferential Context:** Question-answer pairs that require reasoning about the entire audio scene, not just isolated events.

## 2. Annotation Schema & Structure

Each audio clip in this dataset is accompanied by a detailed JSON file with the following structure:

* **`metadata`**: Includes `audio_filename`, `duration_seconds`, `language`, and a `scene_description`.
* **`annotations`**: A list of timestamped events, which can be of two types:
    * **`speech_transcript`**: Contains the transcribed text and a `speaker_id`.
    * **`non_speech_event`**: Contains a descriptive `event_label` (e.g., `vehicle_horn_auto_rickshaw`).
* **`speaker_details`**: Provides more information about each unique `speaker_id` (e.g., gender, role).
* **`Youtube_pairs`**: A set of complex, inferential questions and detailed answers based on the full context of the audio clip.

A sample of the JSON structure can be found in the `examples` folder.

## 3. Methodology

This dataset is created using a meticulous manual annotation process to ensure the highest quality. Each clip is carefully transcribed and annotated by human 
